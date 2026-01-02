# contactus-sweet-corner
<?php
include "config.php";

if(isset($_POST['send'])){
    $name = $_POST['name'];
    $email = $_POST['email'];
    $message = $_POST['message'];

    $sql = "INSERT INTO contacts(name,email,message) 
            VALUES('$name','$email','$message')";
    if(mysqli_query($conn,$sql)){
        echo "<script>alert('Message sent successfully!');</script>";
    }else{
        echo "Error: ".mysqli_error($conn);
    }
}
?>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>sweet</title>
    <link rel="stylesheet" href="style.css">
</head>

<body>
     <header>
    <nav class="navbar">
            <a href="#"class="nav-logo">
        <h2 class="logo-text">🧇The Sweet Corner</h2>
    
    
           </a>
           <ul class="nav-menu">

        <li class="nav-item">
            <a href="index.php"class="nav-link">Home</a>

        </li>
        <li class="nav-item">
            <a href="aboutus.php"class="nav-link">About Us</a>

        </li>
        <li class="nav-item">
            <a href="menu.php"class="nav-link">Menu</a>

        </li>
        <li class="nav-item">
            <a href="Reviews.php"class="nav-link">Reviews</a>

        </li>
        <li class="nav-item">
            <a href="contactus.php"class="nav-link">contact us
</a>

        </li>
    

         </ul>   
        
 

    </nav>
   </header>




<section class="contact-container">

    <!-- Contact Information -->
   
    <div class="contact-info">
        <h2>Contact Information</h2>
        <p><strong>📍 Address:</strong> Rue 21 xxx, Skikda</p>
        <p><strong>📞 Phone:</strong> 05 xx xx xx xx</p>
        <p><strong>📧 Email:</strong> thesweetcorner21@email.com</p>

        <h3>🕒 Working Hours</h3>
        <ul>
            <li>Saturday – Thursday: <span>08:00 AM – 10:00 PM</span></li>
            <li>Friday: <span>02:00 PM – 10:00 PM</span></li>
        </ul>
    </div>

    <!-- Contact Form -->
    <!-- Form -->
<form action="" method="POST" class="contact-form">
<label><b>Name:</b></label>
<input type="text" name="name" required><br><br>
<label><b>Email:</b></label>
<input type="email" name="email" required><br><br>
<label><b>Message:</b></label>
<textarea name="message" required></textarea><br><br>
<button type="submit" name="send">Send</button>
</form>

</section>

<!-- Map Section -->
<section class="map-section">
    <h2>📍 Find Us</h2>
    <div class="map-container">
       <iframe
  src="https://www.google.com/maps?q=Skikda,+Algeria&output=embed"
  loading="lazy"
  allowfullscreen>
</iframe>
    </div>
</section>




   
<footer class="footer">
  <div class="footer-box">
    <h3>The Sweet Corner</h3>
    <ul>
      <li>Home</li>
      <li>About Us</li>
      <li>Menu</li>
      <li>Reviews</li>
      <li>Contact Us</li>
    </ul>
  </div>

  <div class="footer-box">
    <h3>Contact</h3>
    <p>Email: thesweetcorner21@gmail.com</p>
    <p>Phone: 05 xx xx xx xx</p>
    <p>Address: Rue 21 xxx, Skikda</p>
  </div>

  <div class="footer-box">
    <h3>Suivez-nous</h3>
    <ul>
      <li>Facebook</li>
      <li>Instagram</li>
    </ul>
  </div>
  
</footer>
 <div class="footer-bottom">
    <p><b>© 2026 My Shop. The Sweet Corner.</b></p> </div>

    
</body>
</html>
