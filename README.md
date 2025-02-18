# **Step-by-Step Guide: Kafka Producer & Kafdrop UI Verification**

## **1. How to start** 
1. Run Command:
   ```sh
    docker-compose up -d

3. Run Command:
   ```sh
   docker-compose ps

---

## **2. Open Kafdrop UI**
1. Ensure your **Kafka and Kafdrop** services are running.
2. Open a browser and go to:  
   **[http://localhost:9000](http://localhost:9000)**
3. You should see the **Kafdrop UI Dashboard**.

---

## **3. Create a Kafka Topic via Kafdrop**
1. Click on **Create New Topic** in the Kafdrop UI.
2. Enter a **Topic Name** (e.g., `test-topic`).
3. Set:
   - **Partitions** = `1`
   - **Replication Factor** = `1`
4. Click **Create**.

---

## **4. Run Kafka Producer and Send Messages**
1. Open a **terminal**.
2. Run the Kafka producer:
   ```sh
   docker exec -it kafka kafka-console-producer.sh --broker-list localhost:9093 --topic test-topic

## **5. Verify Messages in Kafdrop UI**
1. Go back to **Kafdrop UI**.
2. Click on the **test-topic** you created.
3. Click on **View Messages**.
4. You should see the messages you sent from the producer.

##Note: Tested only on MacBook Pro M1 with Docker Desktop
