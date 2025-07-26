owner of this 

### t.me/gangsterhack

**Note:** Download the zip file and ensure it's in the `~/storage/downloads` directory.

### Step 1: Set Up Termux
1. **Grant storage permissions:**
   ```sh
   termux-setup-storage
   ```

2. **Install necessary packages:**
   ```sh
   pkg install unzip
   ```

3. **Unzip the file:**
   ```sh
   unzip ~/storage/downloads/Termux_Tool.zip -d ~/
   ```

4. **Make the script executable and run it:**
   ```sh
   chmod +x termux.sh
   ```
   ```
   ./termux.sh
   ```

### Step 2: Install Everything You Need
1. **Paste these commands in Termux:**
   ```sh
   termux-setup-storage
   pkg install unzip
   unzip ~/storage/downloads/Termux_Tool.zip -d ~/
   chmod +x termux.sh
   ./termux.sh
   ```

These commands will automatically download everything you need.

### Step 3: Start the Scan
1. **Run the script:**
   ```sh
   python2 analiz.py
   ```

2. **Enter a domain when prompted:** Input the domain you want to scan.

This script will use `subfinder`, `assetfinder`,`findomain` and `sublister` to find all domains and save them in `subdomains.txt`. This scan might take some time, so please be patient.

### Step 4: After the Scan
1. **Switch to the line without an internet package.**
2. **Run the script:**
   ```sh
   python bugscanner.py
   ```

This script will remove duplicates from the collected hosts, scan the file, and save all HTTP responses, displaying them on the screen. This includes Cloudflare and CloudFront responses.

The HTTP headers are set to capture any response between 2xx and 5xx status codes, ensuring it logs all responses from the hosts.

**Hope you find something interesting!**

https://github.com/projectdiscovery/subfinder
