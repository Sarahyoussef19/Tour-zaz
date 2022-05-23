<template>
    <h3 class="conciertos-disponibles"> Conciertos disponibles son :{{ conciertos.length }}</h3>
    <n-card title="Zaz Tour" class="n-card">

        <n-timeline>
            <template v-for="concierto in conciertos_map">
                <n-timeline-item :type="concierto.canceled ? 'error' : 'success'"
                    :line-type="concierto.is_future ? 'dashed' : 'default'">
                    <n-button :disabled="concierto.sold_out" v-if="concierto.is_future">Comprar Entradas</n-button>
                    <template #header>
                        {{ concierto.city }} , <em>{{ concierto.venue }}</em>
                    </template>

                    <template #footer>
                        {{ concierto.date }} . {{ concierto.country }}
                    </template>

                </n-timeline-item>
            </template>
        </n-timeline>
    </n-card>
</template>

<script >
import axios from 'axios'
import { NTimeline, NTimelineItem, NCard, NButton } from 'naive-ui'
export default {
    data() {
        return {
            conciertos: []
        }
    },
    async created() {
        let respuesta = await axios.get('https://conciertos-curso.s3.eu-west-1.amazonaws.com/zaz.json')
        this.conciertos = respuesta.data
        console.log(this.conciertos_map)
    },
    computed: {
        conciertos_ordenados() {
            let conciertos_temp = this.conciertos
            conciertos_temp = conciertos_temp.sort(function (x, y) {
                if (x.date < y.date) { return -1; }
                if (x.date > y.date) { return 1; }
                return 0;

            })
            return conciertos_temp
        },
        conciertos_map() {
            let conciertos_transformados = this.conciertos_ordenados
            conciertos_transformados = conciertos_transformados.map(
                (concierto) => ({
                    city: concierto.city,
                    venue: concierto.venue,
                    country: concierto.country,
                    date: this.transformar_fecha(concierto.date),
                    lat: concierto.lat,
                    long: concierto.long,
                    canceled: concierto.canceled,
                    sold: concierto.sold,

                    sold_out: concierto.sold === 100,
                    is_future: new Date() < new Date(concierto.date),
                    allow_purchase: !concierto.canceled && !concierto.sold !== 100
                })
            )
            return conciertos_transformados
        }
    },
    methods: {
        transformar_fecha(fecha) {
            let fecha_humana = new Date(fecha)
            const opciones_fecha = { dateStyle: 'full', timeStyle: 'long', timeZone: 'UTC' }
            fecha_humana = new Intl.DateTimeFormat('es-Es', opciones_fecha).format(fecha_humana)
            return fecha_humana
        }
    },
    components: { NTimeline, NTimelineItem, NCard, NButton }

}

</script>

<style>
.conciertos-disponibles {
    background-color: black;
    color: white;
    padding: 10px;
    border-radius: 5px;
    cursor: pointer;
}

.conciertos-disponibles:hover {
    background-color: #eee;
    color: black;
}

.n-card {
    padding: auto;
    margin-left: 60px;
}
</style>