## Viewing a file on a S3 Bucket

The're are multiple ways to access files on a SS3 Bucket. Here are some of the ways to do it.

## Objeet URL

Click one of your files then navigate to the ```Properties``` tab. and click the link under the ```Block URL```.
<br>
<img width="1388" height="494" alt="image" src="https://github.com/user-attachments/assets/b8cda624-0eff-452a-a754-f8b64785c815" />
<br>

You might get a similar error like this:
<br>
<img width="776" height="161" alt="image" src="https://github.com/user-attachments/assets/68ee3919-43d0-4679-ae60-d3339fd5d232" />
<br>

*Question:* Why is  it saying ```access denied```?
<br>

*Answer:* When we click that link, what is actually happening is that it is opening the file from the perspective of public user which is unauthenticated and block by default when we first created our bucket. We can see that policy under the ```Permission``` tab, ```Block public access (bucket settings)```.
<br>
<img width="875" height="437" alt="image" src="https://github.com/user-attachments/assets/5e1ef6a7-81d0-48bd-a8fd-3afccad8c21c" />
<br>

To open the file that we are authenticated with, select the ```Open``` icon.
<br>
<img width="646" height="86" alt="image" src="https://github.com/user-attachments/assets/f434f6ff-8c3a-425d-895a-23c6c7c2fce6" />
<br>


## Creating a Folder

Another way of a accessing a file on our Bucket is to put it inside a folder. On the this demo, we will name our folder as ```test```. The select ```Create folder```.
<br>
<img width="1664" height="766" alt="image" src="https://github.com/user-attachments/assets/38cf99da-b11a-46af-a4f8-96fc6182e0fa" />
<br>

Next, select a file by clicking the check box, click on ```Actions``` and select ```Move```.
<br>
<img width="232" height="460" alt="image" src="https://github.com/user-attachments/assets/3f38cb14-2724-4f87-9f0f-b5801f84554f" />
<br>
<br>

Under the ```Destination``` section, you can manually input the file path of the destination or in this case, we will be using the ```Browse S3``` for easier navigation.
<br>
<img width="1631" height="571" alt="image" src="https://github.com/user-attachments/assets/bd701574-9d3a-4ddd-8880-87370dd31c0e" />
<br>
<br>

Select the ```Test``` folder that we've created then click ```Choose Destination```. Scroll down on the lower right and click ```Move```.
<br>
<img width="1784" height="346" alt="image" src="https://github.com/user-attachments/assets/5b5a71ef-6ede-455e-bd74-1119e8d761e4" />
<br>
<br>

it may take some time depending on the size of the file. Wait for it to finished.
<br>
<img width="969" height="60" alt="image" src="https://github.com/user-attachments/assets/87b3ea15-cf61-486f-9841-901d06b8a483" />
<br>

<br>
<img width="530" height="51" alt="image" src="https://github.com/user-attachments/assets/c61fc154-74ae-4c93-8d00-c61650aa2d41" />
<br>
<br>



***NOTE:*** S3 actually **does not** have a concepts of folders, it just mimics the it's functionality. For more in-depth info, you visit this [link](https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-folders.html)


