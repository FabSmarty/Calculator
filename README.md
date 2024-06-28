<!DOCTYPE html>
<html lang="en">
<head>
<title>Styled Calculator</title>
<style>
    body {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
        background-color: #f0f0f0;
        font-family: Arial, sans-serif;
    }
    .calculator {
        background-color: #6981D6;
        border: 2px solid #ccc;
        border-radius: 10px;
        box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);
        padding: 20px;
        width: 300px;
    }
    .calculator input[type="text"] {
        width: calc(100% - 20px);
        padding: 10px;
        margin: 10px 0;
        border: 1px solid #ccc;
        border-radius: 5px;
        font-size: 16px;
    }
    .calculator button {
        background-color: #0080ff;
        border: none;
        border-radius: 5px;
        color: #fff;
        padding: 10px;
        margin: 5px;
        cursor: pointer;
        width: calc(25% - 10px);
        font-size: 16px;
    }
    .calculator button svg {
        vertical-align: middle;
    }
    .calculator button:hover {
        background-color: #005bb5;
    }
    .calculator .equal {
        background-color: #ff0080;
    }
    .calculator .equal:hover {
        background-color: #b50050;
    }
    .calculator .clear {
        background-color: #8000ff;
    }
    .calculator .clear:hover {
        background-color: #5700b5;
    }
    .calculator .add {
        background-color: #0000F5;
    }
    .calculator .add:hover {
        background-color: #0000b5;
    }
    .calculator .subtract {
        background-color: #33df20;
    }
    .calculator .subtract:hover {
        background-color: #28b514;
    }
    .calculator .multiply {
        background-color: #ff0080;
    }
    .calculator .multiply:hover {
        background-color: #b50050;
    }
    .calculator .divide {
        background-color: #FF1100;
    }
    .calculator .divide:hover {
        background-color:#FF1100;
    }
 .help-box {
        display: none;
        background-color: #fff;
        border: 2px solid #ccc;
        border-radius: 10px;
        padding: 20px;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 80%;
        max-width: 300px;
        text-align: center;
    }
    .help-box p {
        font-size: 16px;
        color: #333;
    }
    .help-box button {
        background-color: #8000ff;
        border: none;
        border-radius: 5px;
        color: #fff;
        padding: 10px;
        margin-top: 20px;
        cursor: pointer;
        width: 100%;
        font-size: 16px;
    }
    .help-box button:hover {
        background-color: #5700b5;
    }
</style>
</head>
<body>


<div class="calculator">
    <form name="form" method="post">
<style>
body {
        background-color:#FFF700;
    }

   	 
    }
    td {
	font-face: Algerian;
        font-size: 20px;
        color:#122EFF;

    }
 </style>

<tr><td><marquee direction="right"><svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960" width="24px" fill="#0000F5"><path d="M240-160v-80l260-240-260-240v-80h480v120H431l215 200-215 200h289v120H240Z"/></svg> CALCULATOR <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960" width="24px" fill="#ff0080"><path d="M320-240h60v-80h80v-60h-80v-80h-60v80h-80v60h80v80Zm200-30h200v-60H520v60Zm0-100h200v-60H520v60Zm44-152 56-56 56 56 42-42-56-58 56-56-42-42-56 56-56-56-42 42 56 56-56 58 42 42Zm-314-70h200v-60H250v60Zm-50 472q-33 0-56.5-23.5T120-200v-560q0-33 23.5-56.5T200-840h560q33 0 56.5 23.5T840-760v560q0 33-23.5 56.5T760-120H200Zm0-80h560v-560H200v560Zm0-560v560-560Z"/></svg></marquee></td></tr>


        <input type="text" name="t1" placeholder="Enter 1st Number" size="20"><br>
        <input type="text" name="t2" placeholder="Enter 2nd Number" size="20"><br>
        <input type="text" name="t3" placeholder="Answer" size="30" readonly><br>

        <button type="button" name="b1" class="add" onclick="func1()">
            <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960" width="24px" fill="#ffffff">
                <path d="M440-440H200v-80h240v-240h80v240h240v80H520v240h-80v-240Z"/>
            </svg>
        </button> 

        <button type="button" name="b2" class="subtract" onclick="func2()">
            <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960" width="24px" fill="#ffffff">
                <path d="M200-440v-80h560v80H200Z"/>
            </svg>
        </button>

        <button type="button" name="b3" class="multiply" onclick="func3()">
            <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960" width="24px" fill="#ffffff">
                <path d="m256-200-56-56 224-224-224-224 56-56 224 224 224-224 56 56-224 224 224 224-56 56-224-224-224 224Z"/>
            </svg>
        </button>

        <button type="button" name="b4" class="divide" onclick="func4()">
            <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960" width="24px" fill="#ffffff">
                <path d="M300-520q-58 0-99-41t-41-99q0-58 41-99t99-41q58 0 99 41t41 99q0 58-41 99t-99 41Zm0-80q25 0 42.5-17.5T360-660q0-25-17.5-42.5T300-720q-25 0-42.5 17.5T240-660q0 25 17.5 42.5T300-600Zm360 440q-58 0-99-41t-41-99q0-58 41-99t99-41q58 0 99 41t41 99q0 58-41 99t-99 41Zm0-80q25 0 42.5-17.5T720-300q0-25-17.5-42.5T660-360q-25 0-42.5 17.5T600-300q0 25 17.5 42.5T660-240Zm-444 80-56-56 584-584 56 56-584 584Z"/>
            </svg>
        </button>

        <button type="button" name="b5" class="clear" onclick="func5()">
           <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960" width="24px" fill="#D9D9D9"><path d="m376-300 104-104 104 104 56-56-104-104 104-104-56-56-104 104-104-104-56 56 104 104-104 104 56 56Zm-96 180q-33 0-56.5-23.5T200-200v-520h-40v-80h200v-40h240v40h200v80h-40v520q0 33-23.5 56.5T680-120H280Zm400-600H280v520h400v-520Zm-400 0v520-520Z"/></svg>
        </button>


 
 <button type="button" name="b6" class="help" onclick="func6()">
            <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960" width="24px" fill="#D9D9D9">
                <path d="M478-240q21 0 35.5-14.5T528-290q0-21-14.5-35.5T478-340q-21 0-35.5 14.5T428-290q0 21 14.5 35.5T478-240Zm-36-154h74q0-33 7.5-52t42.5-52q26-26 41-49.5t15-56.5q0-56-41-86t-97-30q-57 0-92.5 30T342-618l66 26q5-18 22.5-39t53.5-21q32 0 48 17.5t16 38.5q0 20-12 37.5T506-526q-44 39-54 59t-10 73Zm38 314q-83 0-156-31.5T197-197q-54-54-85.5-127T80-480q0-83 31.5-156T197-763q54-54 127-85.5T480-880q83 0 156 31.5T763-763q54 54 85.5 127T880-480q0 83-31.5 156T763-197q-54 54-127 85.5T480-80Zm0-80q134 0 227-93t93-227q0-134-93-227t-227-93q-134 0-227 93t-93 227q0 134 93 227t227 93Zm0-320Z"/>
            </svg></button>
    </form>
</div>
</div>

<div class="help-box" id="helpBox">
    <p>Enter numbers to add, subtract, multiply & divide. No alphabet will be calculated in this calculator! For more details Contact : Mr. Suraj Bala (9800228538)!!</p>
    <button onclick="closeHelpBox()">Close</button>
</div>

<script language="javascript">
    function func1() {
        document.form.t3.value = parseInt(document.form.t2.value) + parseInt(document.form.t1.value);
    }
    function func2() {
        document.form.t3.value = parseInt(document.form.t2.value) - parseInt(document.form.t1.value);
    }
    function func3() {
        document.form.t3.value = parseInt(document.form.t2.value) * parseInt(document.form.t1.value);
    }
    function func4() {
        document.form.t3.value = parseInt(document.form.t1.value) / parseInt(document.form.t2.value);
    }
    function func5() {
        document.form.t1.value = "";
        document.form.t2.value = "";
        document.form.t3.value = "";
    }
function func6()
    {
        document.getElementById('helpBox').style.display = 'block';
    }
    function closeHelpBox() {
        document.getElementById('helpBox').style.display = 'none';
    }
</script>

</body>
</html>
