<template>
    <footer>
        <div class="footer">
            <div class="footer-top">
                <ul>
                    <li>
                        <a href="https://www.linkedin.com/in/ashadullaa/" target="_blank">
                            <img src="../assets/images/linkdin.png" alt="">
                        </a>
                    </li>
                    <li>
                        <a href="https://www.facebook.com/ashadulla.allgalib.5" target="_blank">
                            <img src="../assets/images/facebook.png" alt="">
                        </a>
                    </li>
                    <li>
                        <a href="https://github.com/AshadullaAllGalib" target="_blank">
                            <img src="../assets/images/git.png" alt="">
                        </a>
                    </li>

                </ul>
            </div>
            <div class="footer-bottom">
                <p>Copyright © 2024 Ashadulla All Galib. All Rights Reserved.

                    <br>Designed by ASHADULLA
                </p>
            </div>

        </div>
    </footer>
</template>

<script setup>

</script>

<style scoped>
.footer {
    padding: 20px 0;

}

.footer-top ul {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 20px;
    list-style-type: none;
    text-decoration: none;
    padding: 0;
}

.footer-top ul li a {
    text-decoration: none;
    color: black;
    font-size: 12px;
}

.footer-top ul li a img {
    width: 25px;
    border-radius: 100%;
    transition: all ease-in-out.2s;
}

.footer-top ul li a img:hover {
    transform: scale(1.1);
}

.footer-bottom {
    text-align: center;
    padding-top: 20px;
}
</style>