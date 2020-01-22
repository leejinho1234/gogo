<template>
<div>
        <div style="font-size:70px; margin:100px;" align="center">로그인</div>
        <span class="label">
            <div style="width:760px; margin:auto;">
                아이디
                <input type="text" name="user_id" id="user_id" maxlength="20" placeholder="아이디" style="width:760px; height:80px; border-bottom:1px solid gray; margin-bottom:80px;">
            </div>
            <div style="width:760px; margin:auto;">
                비밀번호
                <input type="password" name="user_pw" id="user_pw" maxlength="20" placeholder="비밀번호" style="width:760px; height:80px; border-bottom:1px solid gray; margin-bottom:30px;">
            </div>
            <div style="width:760px; margin:auto;">
                <input type="checkbox" value="id_save" name="id_save">아이디 저장하기
                <a href="#" style="float:right; color: gray; text-decoration: none;">아이디/비밀번호 찾기</a>
            </div>
        </span>
        <div align="center" style="margin-top:100px;">
            <router-link to="/home" tag="button" class="myButton" style="padding:20px 360px;">로그인</router-link><br>
            <router-link to="/join" tag="button" class="myButton" style="padding:20px 349px;">회원가입</router-link>
        </div>
</div>
</template>

<script>
export default {
}
</script>

<style>
.label{
    font-size:20px;
    color:gray;
}
input::placeholder{
    font-size:25px;
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
    text-decoration:none;
    margin: 10px;
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
