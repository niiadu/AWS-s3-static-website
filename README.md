# Static Website Hosted on Amazon s3

## Created and s3 bucket with the name website-1200
<img width="1428" alt="Screenshot 2024-08-05 at 2 59 29 PM" src="https://github.com/user-attachments/assets/c1835dad-aa32-4dd2-827f-a2052cb68d9b">

## Enabling Static Website Hosting
By default static website hosting is disabled until you enable it. So i clicked on the bucket i created, then clicked on properties before i scrolled down to the end, where i saw the website hosting attribute. I click on edit and enabled it.
<img width="1421" alt="Screenshot 2024-08-05 at 3 17 57 PM" src="https://github.com/user-attachments/assets/61c5a8d5-d019-4730-89b9-7fec42f40409">

## Upload the Web application files
i then uploaded the html, css and js files into the bucket, which would serve as the website files.
<img width="1189" alt="Screenshot 2024-08-05 at 3 14 10 PM" src="https://github.com/user-attachments/assets/f7844068-573d-45ff-afea-a46df6ed4670">

## Accessing the website
After uploading the file, i tried to access the website through the bucket website endpoint and i didnt work. There was the need to allow public access for the files uploaded into the bucket
<img width="1023" alt="Screenshot 2024-08-05 at 3 19 39 PM" src="https://github.com/user-attachments/assets/647cd630-5669-4ff2-adba-e87185932fe8">

## Make the files ACL public
After uploading the files, i made each file acl public, so as not to compromise other files uploaded into the bucket later.
<img width="1126" alt="Screenshot 2024-08-05 at 3 09 11 PM" src="https://github.com/user-attachments/assets/02bd6fe2-3dbc-4ffa-bc05-51330bfbf2b1">

## The website is accessible 
After making the files public, i was able to access the website.
<img width="1496" alt="Screenshot 2024-08-05 at 3 09 44 PM" src="https://github.com/user-attachments/assets/5cb9d883-4050-4e4a-86c1-b961bcb26a7c">

## Made few changes
I changed the "Served from Amazon s3" in the html file to "Created by Jonas Adjin-Tettey".
<img width="1503" alt="Screenshot 2024-08-05 at 3 15 28 PM" src="https://github.com/user-attachments/assets/8ddc32f3-06e2-42c0-88f6-ce4777c63360">

# Conclusion
This was how i hosted a static website on amazon s3 for public access.
