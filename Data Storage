<?php
$username = $_POST['username'];
$password = $_POST['password'];

$file = fopen("users.txt", "r");

$loggedIn = false;
while (!feof($file)) {
  $line = fgets($file);
  $lineData = explode(",", $line);
  if ($lineData[0] == $username && $lineData[1] == $password) {
    $loggedIn = true;
    break;
  }
}


fclose($file);


if ($loggedIn) {
  header("Location: dashboard.php");
} else {
  echo "Invalid username or password.";
}
?>
