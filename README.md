This project uses the original SolVerde project from our previous years OOP module and adds a registration, login and password reset functions to the project.

Registration:  (user creates account)
  Validates user inputs (email, phone and password match in particular)
  Creates a salt for each user and salted hash
  Saves the users details (with hashed passwords) into the users.txt file.

Login:  (user sign in)
  Loads the users salt and hash from users.txt
  Rehashes the entered password with the saved salt
  Compares hashes against each other > if valid then login success > brings you to original projects mainGUI

Password Reset:  (user resets password)
  Checks securityQ answer, phone and email address from users.txt
  If all match > opens new GUI for password reset
  Allows user to reset password (both new passwords also check if they match) + generates new salt + hash 
  Updates the user registration info within users.txt
