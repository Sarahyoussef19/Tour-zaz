<template>
    <div class="container">
        <div class="row">
            <img src="../assets/Images/logo.jpeg" alt="logo" class="logo">

        </div>
        <div class="row">
            <div class="col-4">
                <img src="../assets/Images/album1.jpeg" alt="" class="album-photo">
                <h4>BUNDLE 2CD COLLECTOR’S EDITION + PRINTING</h4>
                <p>€25.00</p>
                <button class="add-to-cart">
                    <a href="https://zaz-isa.com/en/zaz/48-pack-double-cd-collector-lithographie.html">
                        Add To Card
                    </a>
                </button>
            </div>
            <div class="col-4">
                <img src="../assets/Images/album2.jpeg" alt="" class="album-photo">
                <h4>VINYLE ZAZ ISA</h4>
                <p>€20.00</p>
                <button class="add-to-cart">
                    <a href="https://zaz-isa.com/en/zaz/50-new.html">
                        Add To Card
                    </a>
                </button>
            </div>
            <div class="col-4">
                <img src="../assets/Images/album3.jpeg" alt="" class="album-photo">
                <h4>VINYLE ZAZ ISA</h4>
                <p>€15.00</p>
                <button class="add-to-cart">
                    <a href="https://zaz-isa.com/en/zaz/51-bundle-2cd-collectors-edition-printing.html">
                        Add To Card
                    </a>
                </button>
            </div>
        </div>
        <div class="row footer">
            <div class="col-3">
                <h5>Account</h5>
                <ul>
                    <li> <a href="#">Manage Your Account</a> </li>
                    <li> <a href="#">Track My Order</a>
                    </li>
                    <li> <a href="#">Order And Return</a>
                    </li>
                    <li> <a href="#">Gift Card</a>
                    </li>
                </ul>
            </div>
            <div class="col-3">
                <h5>Support</h5>
                <ul>
                    <li><a href="#">Help Center</a>
                    </li>
                    <li><a href="#">Fans Club</a>
                    </li>
                    <li><a href="#">Product Question</a> </li>
                    <li><a href="#">Contact Us</a>
                    </li>
                </ul>
            </div>
            <div class="col-3">
                <h5>About Us</h5>
                <ul>
                    <li><a href="#">Career</a>
                    </li>
                    <li><a href="#">Newsletter</a>
                    </li>
                    <li><a href="#">Terms Of Service</a></li>
                    <li><a href="#">Privacy Policy</a>
                    </li>
                </ul>
            </div>
            <div class="col-3">
                <h5>Official Partners</h5>
                <ul>
                    <li><a href="#">Youtube</a>
                    </li>
                    <li><a href="#">Spotify</a>
                    </li>
                    <li><a href="#">Warner Music Group</a></li>
                    <li><a href="#">Sony Music</a>
                    </li>
                </ul>
            </div>

        </div>

    </div>
</template>

<script>

</script>

<style>
.container {
    box-sizing: border-box;

}

.row {
    display: flex;
    border: none;
    justify-content: center;

}

.col {
    max-width: 100%;
    display: block;
}

.logo {
    max-width: fit-content;
    margin: auto;
}

.album-photo {
    max-width: 100%;
}

.add-to-cart {
    background-color: black;
    padding: 10px;
    border-radius: 20px;
    font-size: 12px;
    letter-spacing: 1px;
    font-weight: bold;
    padding: 10px 12px;
    cursor: pointer;
}

a,
ul {
    text-decoration: none;
    color: #a4a8ad;
}
</style>