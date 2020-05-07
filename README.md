# Jenkins

There are 3 jobs in this automation process :

Job1 : for deployment of the code to the testing environment. 

Job2 : for the review of quality assurance team.

Job3 : for deployment of the code to the production environment if it is passed by the quality assurance team.

1. Make a local git repository and the desired index file in it.

2. Create a repository in gitHub and run the following commands in git bash.

    git commit -m "message"

    git remote add origin https://github.com/sunny7898/devopsal.git

    git push -u origin master

3. Now create a new branch using the command - git branch dev(branch_name) and switch to it using command - git checkout dev

4. Now add code files you want to add and run the following commands

    -git add .
  
    -git commit -m message
    
    -git push --all
    
5. Now if you want that the the push is automatically done as soon as any changes are committed , then go to the .git/hooks/ folder inside your local git repository and make a file post-commit there (this file should not have any entension). 

  post-commit :-

    #!/bin/bash

    echo "push"

    git push --all

6. Start jenkins and create new job named job1 for the testing environment and follow the configrations shown in the figure.

![](https://github.com/sunny7898/Jenkins/blob/master/screen_shots/image1.png)

![](https://github.com/sunny7898/Jenkins/blob/master/screen_shots/image2.png)

![](https://github.com/sunny7898/Jenkins/blob/master/screen_shots/image3.png)

7. After this make another job for the Quality Assurance and follow along.

![](https://github.com/sunny7898/Jenkins/blob/master/screen_shots/image4.png)

![](https://github.com/sunny7898/Jenkins/blob/master/screen_shots/image5.png)

![](https://github.com/sunny7898/Jenkins/blob/master/screen_shots/image6.png)

![](https://github.com/sunny7898/Jenkins/blob/master/screen_shots/image7.png)

and finally create a third job that will be deployed only if the second job builds successfully.

![](https://github.com/sunny7898/Jenkins/blob/master/screen_shots/image8.png)

![](https://github.com/sunny7898/Jenkins/blob/master/screen_shots/image9.png)

![](https://github.com/sunny7898/Jenkins/blob/master/screen_shots/image10.png)

![](https://github.com/sunny7898/Jenkins/blob/master/screen_shots/Devops.png)
