# Portainer and Raspberry Pi Setup Instructions(Metabase on ARM64) 

![portainer_screenshot](https://github.com/fusecup/metabase-arm64/assets/2886380/1b7e2f1d-40a7-4073-9a0b-65749ee98bcb)

## Step 1: Navigate to Stacks in Portainer

1. Open your Portainer dashboard.
2. Click on **Stacks** from the sidebar menu.
3. Click on **+ Add stack**.

## Step 2: Create a New Stack with the Following Settings

- Name: `metabase` (make sure you don't reuse that name)
- Build method: `Repository`
- **Repository URL**: `https://github.com/fusecup/metabase-arm64`
- **Repository reference**: `refs/heads/main`
- **Compose path**: `docker-compose.yml`
- In the **Environment variables** section, click on **+ Add environment variable**.
- Add the following environment variables:
- **Name**: `DB_PASS` **Value**: `privatepassword`
- **Name**: `DB_USER` **Value**: `privateuser`

## Step 3: Deploy the Stack

1. Once all the settings are configured, click on **Deploy the stack**.
2. Wait for the stack to be deployed and ensure all services are running.

## Additional Information

- Make sure your Raspberry Pi is connected to the network and has Docker and Portainer installed.
- For detailed instructions on installing Docker and Portainer on Raspberry Pi, refer to the official documentation or tutorials.

### Helpful Links
- [Portainer Documentation](https://docs.portainer.io/)
- [Docker Documentation](https://docs.docker.com/)
- [Setting Up Docker on Raspberry Pi](https://www.raspberrypi.org/documentation/computers/containerization/)

---

Feel free to customize these instructions as needed for your specific setup and requirements.

Based of [Metabase issue for supporting ARM](https://github.com/metabase/metabase/issues/13119) and [loancrate/metabase-arm64](https://github.com/loancrate/metabase-arm64)


### Portainer and Raspberry Pi Setup Instructions
