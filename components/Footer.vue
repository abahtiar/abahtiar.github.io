<template>
    <footer class="footer">
        <button class="btn-act" @click="sendEmail()">
            Let's discuss!
            <a style="display:none" id="send-email-data" href="mailto:hiaribahtiar@gmail.com?subject=Hello Ari"></a>
        </button>
        <nav class="social-icon">
            <a target="_BLANK" href="https://github.com/kewcoder">
                <!-- github -->
                <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 24 24"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z" fill="currentColor"/></svg>
            </a>
            <a target="_BLANK" href="https://www.linkedin.com/in/aribahtiar/">
                <!-- linkedin -->
                <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 24 24"><path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z" fill="currentColor"/></svg>
            </a>
             <a target="_BLANK" href="https://www.upwork.com/freelancers/~017cffa3dc7035c850">
                <!-- upwork -->
                <svg enable-background="new 0 0 2500 2500" width="40" height="40" viewBox="0 0 2500 2500" xmlns="http://www.w3.org/2000/svg"><path d="m2315.4 0h-2130.7c-102 0-184.7 80.2-184.7 179.1v2141.7c0 99 82.7 179.2 184.7 179.2h2130.7c102 0 184.6-80.3 184.6-179.2v-2141.7c0-98.9-82.6-179.1-184.6-179.1z" fill="currentColor"/><path d="m1834.6 1453.7c-98.4 0-190.5-41.7-274.3-109.6l20.4-95.8.9-3.5c18.2-102 75.8-273.3 253-273.3 132.9 0 241 108.3 241 241.3-.4 132.6-108.5 240.9-241 240.9zm0-726.7c-226.4 0-401.9 147.3-473.2 389.5-109-163.7-191.4-360.2-239.7-525.7h-243.6v634.8c0 125.1-101.9 227.1-226.9 227.1s-226.8-102-226.8-227.1v-634.8h-243.7v634.8c-.9 260 210.5 473.4 470.1 473.4s471-213.4 471-473.4v-106.5c47.4 98.9 105.4 198.7 175.9 287.5l-149.3 702.7h249.5l108.1-509.7c94.8 60.8 203.8 98.9 328.8 98.9 267.2 0 484.7-219.2 484.7-486.7-.2-267-217.7-484.8-484.9-484.8z" fill="white" /></svg>
            </a>
        </nav>
    </footer>
</template>
<style>
.footer{
    position: fixed;
    bottom: 0;
    left:0;
    width: 100%;
    box-shadow: 1px 1px 1px #ccc;
    background: white;
    padding: 12px 35px;
    display: flex;
    z-index: 20;
}
.btn-act{
    padding: 20px 40px;
    color:#36F354;
    background: black;
    border:0;
    border-radius: 12px;
    font-size: 18px;
    font-weight: bold;
    cursor: pointer;
}
.btn-act:hover{
   color:#78f38c;
   border-radius: 5px;
   transition: .2s ease-in-out;
   text-decoration: underline;
}
.social-icon{
    padding: 12px 30px;
}
.social-icon a{
     padding: 12px 15px;
}
.social-icon a svg{
    width: 40px;
    height: 40px;
    color: black;
}
.social-icon a svg:hover{
   color:#36F354;
    transition: .2s ease-in-out;
   text-decoration: underline;
}
@media screen and (max-width:512px) {
    .footer{
        padding: 12px;
    }
   .btn-act{
     padding: 10px 20px;
     font-size: 14px;
   }
   .social-icon{
        padding: 10px;
   }
   .social-icon a{
     padding: 0 10px;
   }
    .social-icon a svg{
        width: 24px;
        height: 24px;
    }
}
</style>
<script setup>
const sendEmail = () => {
    // alert("send email")
    document.getElementById("send-email-data").click()
}
</script>