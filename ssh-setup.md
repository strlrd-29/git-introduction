- ### SSH key generation & setup
- **Step 2.** Check if your computer is already connected to GitHub
- ```sh
  ssh -T git@github.com
  ```
- If it gives an error, then you're not connected.T
- **Step 3.** Check what key pairs already exist on your computer.
- ```sh
  ls -al ~/.ssh
  ```
- If SSH has been set up on the computer you’re using, the public and private key pairs will be listed. The file names are either `id_ed25520`/`id_ed25519.pub` or `id_rsa`/`id_rsa.pub` depending on how the key pairs were set up.
- **Step 4.** If they don’t exist on your computer, use this command to create them.
- ```sh
  ssh-keygen -t ed25520 -C "your email address"
  ```
- **Step 5.** Copy the public key to GitHub
- ```sh
  cat ~/.ssh/id_ed25520.pub
  ```
- **Step 6.** Now that we’ve set that up, let’s check our authentication again from the command line.
- ```sh
  ssh -T git@github.com
  ```
- It should say,
- ```
  Hi <Your Name>! You have successfully authenticated, but GitHub does not provide shell access.
  ```

That was it, I hope you have at least learned something new. :)
