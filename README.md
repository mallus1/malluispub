# malluispub
#vuln code

<?php
if (isset($_GET['url'])) {
  $url = $_GET['url'];
  // Attacker has full control over the 'url' parameter
  $image = fopen($url, 'rb');
  header("Content-Type: image/png");
  fpassthru($image);
}
?>
