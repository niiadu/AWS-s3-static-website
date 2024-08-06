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

## Alternatively, I used a bucket policy
You could also use this bucket policy to make the bucket public as well, but this would make all the contents in the bucket public, instead of specific files in bucket.
<img width="1164" alt="Screenshot 2024-08-05 at 4 40 31 PM" src="https://github.com/user-attachments/assets/3ac0c601-283c-4222-a716-04754e70ecc1">

## The website is accessible 
After making the files public, i was able to access the website.
<img width="1496" alt="Screenshot 2024-08-05 at 3 09 44 PM" src="https://github.com/user-attachments/assets/5cb9d883-4050-4e4a-86c1-b961bcb26a7c">

## Created a lifecycle Policy for bucket.
I created a lifecycle policy to transition old version of files into Standard IA and also delete the files after 365 days.
<img width="1192" alt="Screenshot 2024-08-05 at 5 29 34 PM" src="https://github.com/user-attachments/assets/017f135e-d53f-4e57-8451-b66f8839497c">

## Created a different bucket in another region
I created another bucket in the OHIO (us-eat-2) region. This is to aid in adding a replication rules
<img width="1182" alt="Screenshot 2024-08-05 at 5 29 16 PM" src="https://github.com/user-attachments/assets/1defda94-3a0b-4121-ac01-49e09ab261dc">

## Created a replication rule
I created a replication rule to replicate new files added to the website-1200 bucket into the newly created bucket in us-eat-2
<img width="1196" alt="Screenshot 2024-08-05 at 5 29 45 PM" src="https://github.com/user-attachments/assets/6ee7a783-f5cd-4b97-a7cf-437dcf975636">

## Made few changes
I changed the "Served from Amazon s3" in the html file to "Created by Jonas Adjin-Tettey".
<img width="1503" alt="Screenshot 2024-08-05 at 3 15 28 PM" src="https://github.com/user-attachments/assets/8ddc32f3-06e2-42c0-88f6-ce4777c63360">

## Replication rule worked
After the changes in the index.html, it replicated the new file into the newly created bucket in OHIO (eu-eat-2)
<img width="1183" alt="Screenshot 2024-08-05 at 5 29 00 PM" src="https://github.com/user-attachments/assets/a739d766-ea4c-4353-b793-d154f9fb254c">


# Conclusion
This was how i hosted a static website on amazon s3 for public access.
