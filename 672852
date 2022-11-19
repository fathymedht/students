<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="preconnect" href="https://fonts.googleapis.com"> 
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.googleapis.com"> 
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin> 
    <link href="https://fonts.googleapis.com/css2?family=Raleway:wght@200&family=Roboto+Condensed:wght@300;700&display=swap" rel="stylesheet">
    <title> جدول الطلاب </title>
    <style>
    body{
        background-color: whitesmoke;
        font-family: 'Raleway', sans-serif;
    }
    #mother{
        width:100% ;
        font-size: 20px;

    }
    main{
        float:left;
        border: 1px solid grey;
        padding: 5px;

    }
    input{
        padding: 4px;
        border: 2px solid black;
        text-align: center;
        font-size: 17px;
        font-family: 'Raleway', sans-serif;
    }
    aside{
        text-align: center;
        width: 300px;
        float: right;
        border:1px solid black ;
        padding: 10px;
        font-size: 20px;
        background-color: silver;
        color: white;

    }
    #tbl{
        width: 890px;
        font-size: 20px;
        text-align: center;


    }
    #tbl:hover{
        background-color: aqua;
    }
    #tbl th{
        background-color: silver;
        color: black;
        font-size: 20px;
        padding: 10px;
        text-align: center;


    }
    aside button{
        width: 190px;
        padding:8px;
        margin-top: 7px;
        font-size: 17px;
        font-family: 'Raleway', sans-serif;
        font-weight:bold ;




    }   

    </style>
</head>
<body dir='rtl'> 
    <?php 

    #التصال مع قاعده البيانات 
    $host='localhost';
    $user='root';
    $pass='';
    $db='student1';
    $con= mysqli_connect($host,$user,$pass,$db);
    $res=mysqli_query( $con,"select * from student");



    #button variabe --
    $id='';
    $name='';
    $address='';
    if (isset($_POST['id'])){
        $id=$_POST['id'];

    }
    if (isset($_POST['name'])){
        $name=$_POST['name'];
        
    }
    if (isset($_POST['address'])){
        $address=$_POST['address'];
        
    }
    $sqls='';
    if(isset($_POST['Add'])){
        $sqls="insert into student value ($id,'$name','$address')";
        mysqli_query($con,$sqls);
        header("location:db-connect.php");


    }
    if(isset($_POST['Delete'])){
        $sqls="delete from student where name='$name'";
        mysqli_query($con,$sqls);
        header("location:db-connect.php");
        
    }

    
    
    ?>


<div id="mother">
<form method="POST">
<aside>


<!--لوحه التحكم -->  


<div id="div">
<img src="https://www.my-mentor.com.au/assets/images/lms-images/login-lady.png" alt="لوجو الموقع" width='250'>
<h3>لوحه المدير</h3>
<label> رقم الطالب</label><br>
<input type="text" name="id" id="id"><br>
<label> اسم الطالب </label><br>
<input type="text" name="name" id="name"><br>
<label> عنوان الطالب </label><br>
<input type="text" name="address" id="address"><br><br>
<button name="Add"> اضافه الطالب </button>
<button name="Delete"> حزف الطالب</button>








</div>    
</aside>


<!--عرض بيانات التحكم -->


<main>
<table id="tbl" >
<tr>
<th> الرقم التسلسلى </th>
<th> اسم الطالب</th>
<th> عنوان الطالب </th>


</tr>
<?php 
while ($row =mysqli_fetch_array($res)){
    echo "<tr>";
    echo "<td>".$row['id']."</td>";
    echo "<td>".$row['name']."</td>";
    echo "<td>".$row['address']."</td>";
    echo"</tr>";

}

?>

</table>
</main>
</form>    


</div>   
    
</body>
</html>