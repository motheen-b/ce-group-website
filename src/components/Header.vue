<template>
    <div>
        <div class="header-container">
            <div class="header-items">
                <svg-img>
                    <img src="../assets/email.svg" />
                </svg-img>
                <div class="item" @click="copyText('+1 (604) 555-5555')">
                    +1 (604) 555-5555
                </div>
                <svg-img>
                    <img src="../assets/phone.svg" />
                </svg-img>
                <div class="item" @click="copyText('contact@cegroup.ca')">
                    contact@cegroup.ca
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
    async function copyText(text) {
        await navigator.clipboard.writeText(text);
        alert('Text copied to clipboard: ' + text);
    }
</script>

<style scoped>
    .header-container {
        display: flex;
        justify-content: flex-end;
        padding: 0 0px;
        height: 40px;        
        background-color: #0E0E0E;
        /* border: 2px solid red; */
    }
    .header-items {
        display: flex;
        margin: 10px ;
        align-items: center;
        /* border: 2px solid white; */
    }
    .item {
        margin: 8px 8px;
        color: #FFFFFF;
    }
    .item:hover {
        cursor: pointer;
        text-decoration: underline;
    }
    .svg-img {
        width: 16px;
        height: 16px;
        display: inline-block; /* Ensure it stays inline with text */
        vertical-align: middle; /* Align vertically with text */
        margin: 0; /* Adjust as needed */
        padding: 0; /* Adjust as needed */
    }
    .svg-img img {
        width: 16px;
        height: 16px;
        display: block; /* Remove extra space at the bottom */
        margin: 0; /* Adjust as needed */
        padding: 0; /* Adjust as needed */
    }
</style>