<template>
    <form>
        <label>Email</label>
        <input type="email" required v-model="email">

        <label>Password</label>
        <input type="Password" required v-model="password">

        <label>Age: </label>
        <select v-model="age">
            <option value="-18"> - 18 Years Old</option>
            <option value="+18"> + 18 Years Old</option>
        </select>



        <div class="terms">
            <input type="checkbox" required v-model="terms">
            <label>I Accept Terms And Conditions</label>

        </div>
        <div>
            <input type="checkbox" value="newsletter" v-model="preference">
            <label>I Want To Recieve Newsletter</label>
        </div>
        <div>
            <input type="checkbox" value="ofers" v-model="preference">
            <label>I'm Interested In Receiving Offers</label>
        </div>
        <div>
            <input type="checkbox" value="music club" v-model="preference">
            <label>Sign Up for Our Musical Club</label>
        </div>
        <div>
            <button class="sign-in">
                Sign in
            </button>
            <button class="sign-up">
                Sign up
            </button>
        </div>
    </form>
</template>

<script>
export default {
    data() {
        return {
            email: '',
            password: '',
            age: '',
            terms: false,
            preference: [],
            tempSkill: '',
            skills: []
        }
    },
    methods: {

    }
}
</script>

<style>
form {

    max-width: 450px;
    margin: 10px auto;
    background-color: white;
    text-align: left;
    padding: 10px;
    border-radius: 10px;
}

label {
    color: #aaa;
    display: inline-block;
    margin: 25px 0 15px;
    font-size: 0.6em;
    text-transform: uppercase;
    letter-spacing: 2px;
    font-weight: bold;
}

input,
select {
    display: block;
    padding: 10px 6px;
    max-width: 100%;
    box-sizing: border-box;
    border: none;
    border-bottom: 2px solid #ddd;
    color: #555;
}

input[type="checkbox"] {
    display: inline-block;
    width: 16px;
    margin: 0 10px 0 0;
    position: relative;
    top: 1px;
}

.sign-in,
.sign-up {
    display: inline-block;
    margin: 20px 25px 0 0;
    padding: 10px 12px;
    background-color: rgba(107, 183, 218, 0.401);
    border-radius: 20px;
    font-size: 12px;
    letter-spacing: 1px;
    font-weight: bold;
    color: #777;
    cursor: pointer;
}
</style> 