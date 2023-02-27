Lab Report 4
=======
_Sravya Chittuluri_

1. Setup: Delete any existing forks of the repository you have on your account

I looked through my forks on GitHub and deleted any I had of the lab7 repository. I did this by going to my fork, going to settings and scrolling down until I found the delete option. I then deleted any lab7 directories from my ieng6 account by using the command ```rm -r lab7```.

2. Setup: Fork the repository

I navigated to the lab7 repo and forked it.

3. The real deal: Start the timer!

Started the timer!

4. Log into ieng6

I typed in the command ```ssh schittuluri@ieng6.ucsd.edu```. (I'm still having trouble with my course specific account, so I was told to just use this account). 

Keys pressed: ```ssh schittuluri@ieng6.ucsd.edu <enter>```

<img width="695" alt="image" src="https://user-images.githubusercontent.com/75595601/221667116-4f08c792-7938-43f1-896e-4379309c513f.png">

5. Clone your fork of the repository from your Github account

I went to GitHub, into my fork, and copied the SSH key that I set up earlier. Then, I used the command ```git clone git@github.com:04sravya/lab7.git```.

Keys pressed: ```<ctrl-v> git clone git@github.com:04sravya/lab7.git <enter>```

<img width="695" alt="image" src="https://user-images.githubusercontent.com/75595601/221671193-de978d22-b1f9-4eee-8259-70a0f8bc94b7.png">

6. Run the tests, demonstrating that they fail

Next, I change my directory to the lab7 folder and run the compile and run commands for the JUnit tests. I used the reverse-i-search to make finding the commands easier.

Keys pressed: ```cd la <tab> <ctrl-r> javac <enter> <ctrl-r> <up> <up> <up> <up> <up> <enter>```

<img width="946" alt="image" src="https://user-images.githubusercontent.com/75595601/221678546-0684a634-dc72-400d-80b5-8a58f1e67bde.png">

11. Edit the code file to fix the failing test

I enter the Vim code editor using the command ```nano ListExamples.java```, and go through the code to fix the bug. The error is that towards the end of the file, index1 is used instead of index2.

Keys pressed: ```nano Li <tab> <enter> *fix index1 to index2* <ctrl-x> <Y> <enter>```

<img width="934" alt="image" src="https://user-images.githubusercontent.com/75595601/221675210-3bebd250-7cc4-449b-824e-e01c82b202f1.png">

13. Run the tests, demonstrating that they now succeed

I compile the JUnit tests and run them again. Since I already have the commands typed out before, I just use the up arrow key to reach the commands to use them again.

Keys pressed: ```<up> <up> <up> <enter> <up> <up> <up> <enter>```

<img width="946" alt="image" src="https://user-images.githubusercontent.com/75595601/221678903-53665014-b0d9-41c1-b24a-48e8004aaa34.png">

15. Commit and push the resulting change to your Github account (you can pick any commit message!)

I use the git add, commit, and push commands to commit and push my changes onto my account.

Keys pressed: ```git add Li <tab> git commit -m "Updated" <enter> git push```

<img width="946" alt="image" src="https://user-images.githubusercontent.com/75595601/221680446-83b16d6a-24e7-4023-805c-bbb51e91d97a.png">

15. Commit and push the resulting change to your Github account (you can pick any commit message!)
