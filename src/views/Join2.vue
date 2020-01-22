<template>
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
                <img src="https://ifh.cc/g/dmVsF.png" width="800">
            </div>
        </div>
        <div style="width:1800px; margin:auto;">
            <div style="font-size:50px;">회원정보 입력
                <span class="label">
                    <em>(필수)</em>
                    입력사항을 꼭 써주시기 바랍니다.
                </span>
            </div>
            <div class="contents">
                <div style="margin:70px;">
                    <div style="float:left; margin-right:70px;">
                        <span class="label">
                                아이디
                            <em>(필수)</em>
                            <div>
                                <input type="text" name="user_id" id="user_id" maxlength="20" placeholder="아이디" style="width:600px; height:80px; border-bottom:1px solid gray">
                                <input type="button" name="check" id="check" value="중복확인" class="myButton">
                            </div>
                        </span>
                    </div>
                    <div>
                        <span class="label">
                                이름
                            <em>(필수)</em>
                            <div>
                                <input type="text" name="user_name" id="user_name" maxlength="20" placeholder="이름" style="width:760px; height:80px; border-bottom:1px solid gray">
                            </div>
                        </span>
                    </div>
                </div>

                <div style="margin:70px;">
                    <div style="float:left; margin-right:70px;">
                        <span class="label">
                                비밀번호
                            <em>(필수)</em>
                            <div>
                                <input type="password" name="user_pw" id="user_pw" maxlength="20" placeholder="비밀번호" style="width:760px; height:80px; border-bottom:1px solid gray">
                            </div>
                        </span>
                    </div>
                    <div>
                        <span class="label">
                                비밀번호 확인
                            <em>(필수)</em>
                            <div>
                                <input type="password" name="user_pw2" id="user_pw2" maxlength="20" placeholder="비밀번호 확인" style="width:760px; height:80px; border-bottom:1px solid gray">
                            </div>
                        </span>
                    </div>
                </div>

                <div style="margin:70px;">
                    <div style="float:left; margin-right:70px;">
                        <span class="label">
                                닉네임
                            <em>(필수)</em>
                            <div>
                                <input type="text" name="user_nick" id="user_nick" maxlength="20" placeholder="닉네임" style="width:600px; height:80px; border-bottom:1px solid gray">
                                <input type="button" name="check" id="check" value="중복확인" class="myButton">
                            </div>
                        </span>
                    </div>
                    <div>
                        <span class="label">
                                이메일
                            <em>(필수)</em>
                            <div>
                                <input type="text" name="user_email" id="user_email" maxlength="20" placeholder="이메일" style="width:600px; height:80px; border-bottom:1px solid gray">
                                <input type="button" name="check" id="check" value="중복확인" class="myButton">
                            </div>
                        </span>
                    </div>
                </div>

                <div style="margin:70px;">
                    <div style="float:left; margin-right:70px;">
                        <span class="label">
                                주소
                            <em>(필수)</em>
                            <div>
                                <input type="text" name="user_zipcode" id="user_zipcode" maxlength="6" style="width:200px; height:80px; border-bottom:1px solid gray">
                                <input type="button" name="check" id="check" value="우편번호" class="myButton">
                                <input type="text" name="user_address" id="user_address" maxlength="20" placeholder="주소" style="width:400px; height:80px; border-bottom:1px solid gray">
                            </div>
                        </span>
                    </div>
                    <div>
                        <span class="label">
                                상세주소
                            <div>
                                <input type="text" name="user_detailedaddress" id="user_detailedaddress" maxlength="20" placeholder="상세주소" style="width:760px; height:80px; border-bottom:1px solid gray">
                            </div>
                        </span>
                    </div>
                </div>

                <div style="margin:70px;">
                    <div style="float:left; margin-right:70px;">
                        <span class="label">
                                핸드폰
                            <em>(필수)</em>
                            <div>
                                <input type="text" name="user_phone1" id="user_phone1" maxlength="3" style="width:240px; height:80px; border-bottom:1px solid gray">
                                -
                                <input type="text" name="user_phone2" id="user_phone2" maxlength="4" style="width:240px; height:80px; border-bottom:1px solid gray">
                                -
                                <input type="text" name="user_phone3" id="user_phone3" maxlength="4" style="width:240px; height:80px; border-bottom:1px solid gray">
                            </div>
                        </span>
                    </div>
                    <div>
                        <span class="label">
                                전화번호
                            <div>
                                <input type="text" name="user_phone1" id="user_phone1" maxlength="3" style="width:240px; height:80px; border-bottom:1px solid gray">
                                -
                                <input type="text" name="user_phone2" id="user_phone2" maxlength="4" style="width:240px; height:80px; border-bottom:1px solid gray">
                                -
                                <input type="text" name="user_phone3" id="user_phone3" maxlength="4" style="width:240px; height:80px; border-bottom:1px solid gray">
                            </div>
                        </span>
                    </div>
                </div>
                <div style="margin:70px;">
                    <div style="float:left; margin-right:70px;">
                        <span class="label">
                                견종/묘종
                            <div>
                                <input type="text" name="user_petkinds" id="user_petkinds" maxlength="20" placeholder="견종/묘종" style="width:760px; height:80px; border-bottom:1px solid gray">
                            </div>
                        </span>
                    </div>
                    <div>
                        <span class="label">
                                반려동물 이름
                            <div>
                                <input type="text" name="user_petname" id="user_petname" maxlength="20" placeholder="반려동물 이름" style="width:760px; height:80px; border-bottom:1px solid gray">
                            </div>
                        </span>
                    </div>
                </div>
            </div>

        <div align="center">
            <input type="button" name="check" id="check" value="회원가입" class="myButton2">
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
.contents{
    width:1800px;
    height:1150px;
    border: 1px solid #80808040;
}
.label{
    font-size:20px;
    color:gray;
}
.label em{
    color:red;
    font-style: normal;
}
input::placeholder{
    font-size:25px;
}

.myButton {
    box-shadow:inset 0px 2px 0px -24px #cf866c;
    background-color: white;
    border-radius:4px;
    border:1px solid black;
    display:inline-block;
    cursor:pointer;
    color:black;
    font-family:Arial;
    font-size:20px;
    padding:20px 30px;
    text-decoration:none;
    margin: 10px;
}
.myButton:hover {
    background-color:black;
    color:white;
}
.myButton:active {
    position:relative;
    top:1px;
}

.myButton2 {
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
    margin-top: 60px;
    margin-bottom: 60px;
}
.myButton2:hover {
    background-color:white;
    color:black;
}
.myButton2:active {
    position:relative;
    top:1px;
}

</style>
