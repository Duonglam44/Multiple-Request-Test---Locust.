🚀 Setup test multiple request 🚀

## step 1: Download and setup locust

### Install locust
  - pip3 install locust
### Prebuild locust
  - pip3 install -U --pre locust

## Step 2: 
  - Setup script

  **Example:**

  ```
  from locust import HttpUser, task, between
  class MyUser(HttpUser):
      wait_time = between(1, 3)

      @task
      def my_task(self):
          response = self.client.get("/your-endpoint")
          print(f"Response status code: {response.status_code}")
          print(f"Response content: {response.text}")
  ```

===================

## Document example:

- [Locust medium](https://medium.com/@mithun.kadyada/python-locust-for-load-testing-website-or-endpoint-url-b402eb3dbdf7).
- [Locust documentation](https://docs.locust.io/en/stable/what-is-locust.html).
