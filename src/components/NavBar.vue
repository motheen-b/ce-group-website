<template>
    <div>
        <div class="nav-container">
            <div class="logo">
                <img src="../assets/logo.png" />
            </div>
            <div class="nav-items">
                <div class="item">
                    Home
                </div>
                <div class="item">
                    Services
                </div>
                <div class="item">
                    Gallery
                </div>
                <div class="item">
                    <div class="contact-item">
                        Contact
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto+Slab:wght@400;700');
    .nav-container {
        display: flex;
        height: 80px;
        margin: 0 10px;
        padding: 0 30px;
        /* border: 2px solid black; */
    }
    .nav-items {
        display: flex;
        align-items: center;
        justify-content: flex-end;
        margin: 10px;
        flex-grow: 1;
        /* border: 2px solid black; */
    }
    .item {
        display: inline-flex;
        font-family: 'Roboto Slab', sans-serif;
        font-weight: 500;
        margin: 8px 20px;
        /* border: 2px solid black; */
    }
    .contact-item {
        background-color: #957349;
        padding: 10px 10px;
        border: 2px solid white;
        border-radius: 15px;
        box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.37);
    }
    .contact-item:hover {
        transform: translateY(2px);
    }
    .item:hover {
        cursor: pointer;
        text-decoration: underline;
    }
    .logo {
        padding-top: 15px;
        align-content: center;
        /* border: 2px solid black; */
    }
    .logo:hover {
        cursor: pointer;
    }
    .logo img {
        height: 80%;
    }
</style>