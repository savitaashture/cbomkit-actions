# cbomkit-actions

## Prerequisites

*   [Docker](https://www.docker.com/)
*   [Docker Compose](https://docs.docker.com/compose/)
*   [ngrok](https://ngrok.com/) API gateway

## Setup Instructions

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/PQCA/cbomkit
    ```

2.  **Start the Docker Compose environment:**

    ```bash
    make production
    ```

    **Note:** This command exposes the frontend on port `8001` and the backend on port `8081` by default, running locally.

3.  **Configure ngrok:**

    *   Install and configure ngrok following the [official documentation](https://ngrok.com/docs).
    *   Expose the backend service using ngrok:

        ```bash
        ngrok http http://localhost:8081
        ```

    *   ngrok will provide a forwarding URL, similar to:

        ```
        ngrok

        ⚖️ Load balance anything, anywhere with Endpoint Pools! https://ngrok.com/r/pools

        Session Status                online
        Account                       savitaashture (Plan: Free)
        Update                        update available (version 3.23.0, Ctrl-U to update)
        Version                       3.22.1
        Region                        India (in)
        Latency                       27ms
        Web Interface                 http://127.0.0.1:4040
        Forwarding                    https://b731-2406-7400-61-e4da-f2c5-5d7e-a17f-35b1.ngrok-free.app -> http://localhost:8081
        ```

## CBOM Compliance Examples

This project demonstrates CBOM (Component Bill of Materials) compliance. Below are example repositories:

*   **CBOM Compliant:** [https://github.com/savitaashture/kyberJCE](https://github.com/savitaashture/kyberJCE)
*   **CBOM Non-Compliant:** [https://github.com/savitaashture/client-encryption-java](https://github.com/savitaashture/client-encryption-java)