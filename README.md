# Pi-hole Lab

## Objective

Implement Pi-hole into the home network using a Raspberry Pi to enhance network security.


### Skills Learned

- DNS Sinkhole
- Network Security
- Assigning Static IP Addresses
- Command Line


### Tools Used

- Raspberry Pi (Physical Hardware)
- Pi-Hole (Software)


## Steps

# Step 1 - Download Raspberry PI OS
Use Raspberry Pi Imager to download OS onto SD card.
https://www.raspberrypi.com/software/

<img width="600" height="400" alt="Screenshot 2025-10-06 at 5 24 27 PM" src="https://github.com/user-attachments/assets/207dbd7f-74d4-493b-bcce-1e6ff6bb8af5" />

# Step 2 - Turn on Raspberry Pi
Insert the SD card with the installed OS into your Raspberry Pi and turn it on. 
Connect your Raspberry Pi through Ethernet or WiFi.

# Step 3 - Connect to Raspberry Pi
Connect to your Raspberry Pi using SSH over the command line (e.g., ssh username@IP-address).

Ensure Raspberry PI OS is updated (e.g., Sudo apt update && sudo apt upgrade).

<img width="600" height="400" alt="Screenshot 2025-10-06 at 5 31 08 PM" src="https://github.com/user-attachments/assets/e4947749-7ee4-49ca-8bc4-e4a132a33ebe" />

# Step 4 - Assign a Static IP to your Raspberry Pi
Multiple ways to do this, but I used the nmtui command(e.g., nmtui).
Once the interface is up, go to "edit connection".
Go to IPv4 and change from "Automatic" to "Manual".
Assign your device the desired static IP address (Ensure that it falls outside the IP addresses your router assigns).

# Step 5 - Install Pi-hole
Use the command line to install Pi-hole (e.g., curl -sSL https://install.pi-hole.net | bash).
Go through the initial setup process for Pi-hole.

# Step 6 - Access Pi-hole Admin
Navigate to hattp://pi-hole IP address/admin

<img width="600" height="400" alt="Screenshot 2025-10-06 at 12 40 58 PM" src="https://github.com/user-attachments/assets/e2478ed8-6caa-472f-9ce9-c690b59f6792" />

# Step 7 - Add Block Lists to Pi-hole
You can add more block lists to Pi-hole by navigating to "lists".
https://firebog.net/ is a great resource to find block lists to add to your Pi-hole.

<img width="600" height="400" alt="Screenshot 2025-10-06 at 4 18 16 PM" src="https://github.com/user-attachments/assets/4ca96b9c-6e5b-4ab0-9f18-ebe78e46132a" />

Use "update gravity" under the tools section to update the block list once you are happy with it.

<img width="600" height="400" alt="Screenshot 2025-10-06 at 4 25 07 PM" src="https://github.com/user-attachments/assets/a1e02698-d372-40eb-8081-5df84388b2d5" />

# Step 8 - Configure DNS for Router or Clients
I chose to change my router's DNS settings. You can also manually configure each client's DNS settings, but it is typically better to change the router's settings for scalability reasons.

<img width="600" height="100" alt="Screenshot 2025-10-06 at 4 57 36 PM" src="https://github.com/user-attachments/assets/b88bd0ef-a97a-4a81-bca5-2c293d0df5a7" />

Once DNS settings are changed, you should start seeing traffic coming into your Pi-hole.

<img width="600" height="400" alt="Screenshot 2025-10-06 at 5 01 14 PM" src="https://github.com/user-attachments/assets/47b9ba82-0573-4212-966f-8b8e5113592a" />

Pi-hole should be up and running! There are settings you can adjust in the Pi-hole admin interface to enhance your security further.







