
# 💯Basic login system with validation + Dashboard💯

This program takes a username and password from the user, checks the credentials, and responds based on whether they're valid or not.

![Static Badge](https://img.shields.io/badge/Python-3.12-blue?style=for-the-badge&link=https%3A%2F%2Fwww.python.org%2Fdownloads%2Frelease%2Fpython-3128%2F)



## Deployment 
Repository can be deployed locally **or** through Streamlit and GitHub;

Assuming you have [Git](https://git-scm.com/downloads), [Pip](https://pip.pypa.io/en/stable/installation/) and [Python](https://www.python.org/downloads/) 3.0 or later installed already

### Local (Windows)




#### Steps:


1. Clone this repository

    ```
    git clone https://github.com/alfie-bb/loginFTP.git
    ```
2. Cd into the `local` folder
    ```
    cd local
    ```
3. Install [Streamlit](https://streamlit.io) + dependencies

    ```
    pip install -r requirements.txt
    ```
4. Start FTP server

    ```
    python ftp.py
    ```
5. Start `main.py` - Separate CLI
    ```
    streamlit run main.py --server.port 80
    ```

#### To use an external FTP server, edit the respective variables in `main.py` with the credentials of the server. - Note: If the **external** server doesn't have the `ftp_files` folder already, you will have to create one, as well as paste a `userlist.csv` file inside of it. I recommend using the `userlist.csv` file inside the `ftp_files` folder in this repository. 

### Cloud (Streamlit + GitHub + Windows)

#### Note: This method will not host the entire backend in the cloud, you will still have to host your own FTP server locally or use an external one. - For this mode of deployment, you will have to have port 21 forwarded if you're hosting your own FTP server locally.

Assuming you have already created a [Streamlit](https://streamlit.io) account and linked it to your GitHub account, and granted all additional scopes, and have already forwarded port 21 for your machine's internal IP:

#### Steps:


1. Clone this repository
    ```
    git clone https://github.com/alfie-bb/loginFTP.git
    ```
2. Cd into the `cloud` folder
    ```
    cd cloud
    ```
3. Install dependencies

    ```
    pip install -r requirements.txt
    ```
4. Open Command Prompt and enter the `ipconfig` command:
- Copy your IPv4 address
- Paste your IPv4 address inside the empty single quotes on `line 23` of the `ftp.py` file inside the `cloud` folder 

5. Start the FTP server

    ```
    python ftp.py
    ```
6. Fork this repository into your own **private** repository
7. Enter your fork, and navigate into the `cloud` folder. - Once inside, open `main.py` for editing
8. Find the `FTP_HOST` variable, and paste your **public** IPv4 address inside the double quotes. - You can find your public IPv4 address at [whatismyipaddress.com](https://whatismyipaddress.com/)
9. Commit the changes made to `main.py`
10. Go to [streamlit.io](https://streamlit.io) and create an app by clicking the button in the top right, and click the blue "Deploy now" text
11. Paste the GitHub URL for your fork - **THIS WILL ONLY WORK IF YOU HAVE GRANTED STREAMLIT ADDITIONAL SCOPES**
12. Keep branch as `master` , but change the main file path to `cloud/main.py`
13. Set the app URL to whatever you like, then press the `Deploy` button



    


## Features

- File editing through a locally or externally hosted FTP server
- Light/dark mode
- Intuitive, user-friendly interface

## Demo

- [Demo Video](https://github.com/alfie-bb/logi/blob/main/demo.mp4)


## Authors

- [@ThEnaylor](https://github.com/ThEnaylor)
- [@alfie-bb](https://github.com/alfie-bb)



## Acknowledgements

- [ChatGPT](https://chat.openai.com)

