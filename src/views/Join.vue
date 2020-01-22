<template>
    <!-- <img class="img" src="https://ifh.cc/g/OhmhQ.jpg" style="width:100%; height:500px;"> -->
    <div>
            <!----------------------------사진--------------------------------->
        <div class="img">
            <div class="content">
                <h1 align="center">회원가입</h1>
            </div>
        </div>
        <!----------------------------------------------------------------->
        <div align="center"><br>
            <div style="padding: 100px 0px;">
                <h3>회  원  가  입</h3>
                <h1>CREATE YOUT ACCOUNT</h1><br>
                <img src="https://ifh.cc/g/dYPKr.png" width="800">
            </div>
        </div>
        <div align="center">
            <div class="rule1">
                <h2>이용약관</h2><br>
                <div class="rule2">
                </div><br>
                <div align="left" style="font-size:25px;">
                    <input type="radio" name="check" style="margin:10px;">동의합니다.
                    <input type="radio" name="check" style="margin:10px;">동의하지 않습니다.
                </div>
            </div>
            <div class="rule1">
                <h2>개인정보 취급방침</h2><br>
                <div class="rule2">
                </div><br>
                <div align="left" style="font-size:25px;">
                    <input type="radio" name="check2" style="margin:10px;">동의합니다.
                    <input type="radio" name="check2" style="margin:10px;">동의하지 않습니다.
                </div>
            </div>
            <div>
                <router-link to="/join2" tag="button" class="myButton">다음단계</router-link>
                <!-- <input type="button" value="다음단계" class="myButton"> -->
            </div>
        </div>
    </div>
</template>
<script>
export default {
}
</script>
<style>
.img{
    position: relative;
    background-image: url(https://ifh.cc/g/OhmhQ.jpg);
    background-size: 100% 700px;
    height: 700px;
    width:100%;
    }
.content{
    z-index: -1;
    color:white;
    padding: 300px 0px;
}
.rule1{
    display: inline-block;
    margin: 50px;
}
.rule2{
    overflow:auto;
    width:800px;
    height:500px;
    border:1px solid #80808040;
}

.myButton {
    box-shadow:inset 0px 2px 0px -24px #cf866c;
    background-color: black;
    border-radius:4px;
    border:1px solid black;
    display:inline-block;
    cursor:pointer;
    color:#ffffff;
    font-family:Arial;
    font-size:25px;
    padding:20px 40px;
    text-decoration:none;
    margin: 40px;
}
.myButton:hover {
    background-color:white;
    color:black;
}
.myButton:active {
    position:relative;
    top:1px;
}

</style>
