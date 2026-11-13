# Connecting Raspberry Pi to EMQX Cloud
*A Practical Guide to Cloud-Based MQTT Communication*

**Equipment and software:**
- Raspberry Pi with Raspberry Pi OS.
- Internet connection.
- Python 3.
- EMQX Cloud account.
- Paho MQTT Python library.

---

## 1. Introduction to EMQX Cloud

EMQX Cloud provides a hosted MQTT broker that allows IoT devices to exchange messages over the internet.

Unlike a locally installed broker, such as Eclipse Mosquitto, EMQX Cloud runs on remote servers.

This means that your Raspberry Pi can communicate with other devices without needing to host its own MQTT broker.

For this activity, we will use the **EMQX Serverless free tier**.

The current free quota includes:

- 1 million session minutes per month.
- 1 GB of network traffic per month.
- 1 million rule actions per month.

The free quota is subject to EMQX's usage conditions and limits. We will configure the spending limit to zero to avoid charges beyond the free allowance.

---

## 2. Create an EMQX Cloud Account

1. Open the EMQX Cloud website:

   https://www.emqx.com/en

2. Select the option to register for an account.
3. Enter your email address and the requested details.
4. Complete the email verification process.
5. Log in to the EMQX Cloud Console.

You may be asked to complete mobile verification during registration.

<img width="1903" height="1073" alt="image" src="https://github.com/user-attachments/assets/cc265aa9-855b-4024-b81f-53adf9bac637" />


---

## 3. Create Your First MQTT Deployment

After logging in, you need to create a project and an MQTT broker.

### 3.1 Create a project

1. Open the Overview page.
2. Select **New Project**.
3. Enter a project name, for example:

   `University-IoT-Lab`

4. Add a short description if requested.
5. Select **Confirm**.

### 3.2 Create a Serverless deployment

1. Open your newly created project.
2. Select **New Deployment**.
3. Choose the **Serverless** plan.
4. Configure your deployment:
   - Deployment name: `student01-broker`
   - Region: Select a region close to your location.
   - Spend limit: Leave it at `0` to restrict usage to the free quota.
5. Review the deployment details.
6. Accept the usage terms.
7. Select **Deploy**.

Wait until the deployment status changes to **Running**.

Your MQTT broker is now ready.

> **Insert Screenshot 2:** Serverless deployment creation.

> **Insert Screenshot 3:** Your deployment showing Running status.

---

## 4. Create MQTT Credentials

Your Raspberry Pi needs authentication details to connect to the broker.

1. Open your deployment.
2. Navigate to **Access Control**.
3. Select **Authentication**.
4. Select **Add**.
5. Enter the following:
   - Username: `student01`
   - Password: Create a secure password.
6. Select **Confirm**.

Keep your credentials safe. You will need them when connecting your Raspberry Pi.

> **Insert Screenshot 4:** Authentication configuration.

---

## 5. Retrieve Your MQTT Connection Details

Open the **Overview** page of your deployment.

You should find the following information:

| Parameter | Description |
|---|---|
| Host | Your unique EMQX broker address |
| Port | `8883` |
| Protocol | MQTT over TLS |
| Username | Your MQTT username |
| Password | Your MQTT password |

Your broker address will look similar to:

`xxxxxxxxxx.emqxsl.com`

Use the actual hostname displayed in your account.

### Download the CA certificate

EMQX Serverless requires encrypted connections.

1. Find the CA Certificate option in your deployment Overview.
2. Download the certificate.
3. Save it somewhere accessible from your Raspberry Pi.

You will need this certificate to establish a secure connection.

> **Insert Screenshot 5:** Deployment connection details and CA certificate download.

**Important:** Do not use port 1883 for this Serverless deployment. Use port 8883 with TLS encryption.
