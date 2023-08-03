# Elastic Beanstalk dashboard

![image](https://github.com/nthduc95/cd12099-Full-Stack-Apps-AWS/assets/119287881/9036d7ed-846f-47c0-9c0d-c44601e240c9)
![image](https://github.com/nthduc95/cd12099-Full-Stack-Apps-AWS/assets/119287881/9866882b-71ac-4e2b-9aa0-d84745e18e5f)

# Endpoint URL for a running elastic beanstalk deployment
- Root endpoint to display simple message.

  http://cd12099-full-stack-apps-aws-dev.us-east-1.elasticbeanstalk.com/
  ![image](https://github.com/nthduc95/cd12099-Full-Stack-Apps-AWS/assets/119287881/b8aa36d5-0cee-4837-805b-41618e73889e)

- Endpoint to filter an image from a public url.

  1. Query parameter image_url is empty -> return status 400 and message error.

    http://cd12099-full-stack-apps-aws-dev.us-east-1.elasticbeanstalk.com/filteredimage?image_url=
    ![image](https://github.com/nthduc95/cd12099-Full-Stack-Apps-AWS/assets/119287881/a2ffe095-fac1-4bda-b00d-550b862d9ada)

  2. Query parameter image_url is not valid url -> return status 400 and message error.

    http://cd12099-full-stack-apps-aws-dev.us-east-1.elasticbeanstalk.com/filteredimage?image_url=aaaaaa
    ![image](https://github.com/nthduc95/cd12099-Full-Stack-Apps-AWS/assets/119287881/7c31e75a-eaf3-4510-9d78-0984ee543cf4)

  3. Query parameter image_url is not a image -> return status 500 and message error.

    http://cd12099-full-stack-apps-aws-dev.us-east-1.elasticbeanstalk.com/filteredimage?image_url=https://www.google.com.vn/
    ![image](https://github.com/nthduc95/cd12099-Full-Stack-Apps-AWS/assets/119287881/887970fd-e0af-4211-ba28-967959a4ca9a)

  4. Query parameter image_url is valid -> return status 200 and response image.

    http://cd12099-full-stack-apps-aws-dev.us-east-1.elasticbeanstalk.com/filteredimage?image_url=https://blog.logrocket.com/wp-content/uploads/2020/09/documenting-express-js-api-swagger.png
    ![image](https://github.com/nthduc95/cd12099-Full-Stack-Apps-AWS/assets/119287881/3f3eace3-976f-442b-8dbe-2b98459765c0)

    http://cd12099-full-stack-apps-aws-dev.us-east-1.elasticbeanstalk.com/filteredimage?image_url=https://upload.wikimedia.org/wikipedia/commons/b/bd/Golden_tabby_and_white_kitten_n01.jpg
    ![image](https://github.com/nthduc95/cd12099-Full-Stack-Apps-AWS/assets/119287881/8947eea7-503c-454f-ba88-e97902350b08)

