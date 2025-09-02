# Using Git to Track and Manage Changes for a Simple Form
Go into your github account and create a repository , name is **simple-form**
![alt text](<picture documents/simple form repo.png>)




## 1. Clone the existing GitHub repository called simple-form to your local machine
git clone https://github.com/yourusername/simple-form.git

![alt text](<picture documents/git clone simple form.png>)


 cd simple-form
![alt text](<picture documents/cd simple form.png>)



## 2. Stage the Form File:
Place the client's HTML form file (form.html) and CSS (style.css) in this folder and save.
![alt text](<picture documents/html file view.png>)

![alt text](<picture documents/css file view.png>)


### Use Git to add the form.html and style.css files to the staging area:
git add form.html style.css
![alt text](<picture documents/git add html and css file.png>)



### 3. Commit the staged files with a message:
git commit -m "Initial commit for simple form"
![alt text](<picture documents/git commit simple form.png>)



### 4. Push the initial commit to the remote repository:
git push origin main
![alt text](<picture documents/git push origin main.png>)



#### 5. Your client requests some updates to the form. You modify form.html to include an additional field for a phone number and update the styling in style.css.

adding an additional field  for phone number 
![alt text](<picture documents/aadding a phone number field.png>)


updating the styling in stle.css
![alt text](<picture documents/updating css style.png>)

###### After making these changes, stage and commit the updated files with a message:
git add form.html style.css
git commit -m "Added phone number field and updated styles"
![alt text](<picture documents/git add html and css file.png>)


![alt text](<picture documents/added phone and updated style.png>)



#### 6. Push your latest changes to the remote repository:
git push origin main
![alt text](<picture documents/git pushing new changes.png>)

#### 7. After working on several features and fixes, view the Git history to check all the changes you've made:
![alt text](<picture documents/git log.png>)


#### 8. Your client realizes that one of the previous changes introduced a bug in the form submission process. You need to revert form.html to the last working version. First, find the commit hash of the last working version using git log, then run:
git checkout <commit-hash> -- form.html


#### 9. Your client wants to experiment with adding a CAPTCHA feature to the form. Create a new branch called feature-add-captcha and switch to it:
![alt text](<picture documents/creating faetre captcha view.png>)

git checkout -b feature-add-captcha
![alt text](<picture documents/git checkout feature branch.png>)

*Make the necessary changes for the CAPTCHA feature, then stage and commit them:**
![alt text](<picture documents/view of the captcha file.png>)

git add form.html

git commit -m "Added CAPTCHA feature"
![alt text](<picture documents/git add and commit captcha feature.png>)

Merge the changes back into the main branch:
git checkout main/
git merge feature-add-captcha
![alt text](<picture documents/switch and merge feature branch to main branch.png>)




#### 10. After merging, push the updated main branch to the remote repository:
git push origin main
![alt text](<picture documents/Screenshot 2025-08-25 185330.png>)


#### 11. You accidentally made some unwanted changes to style.css that you haven't committed yet. Discard these local changes and revert the file to its previous state:
git checkout -- style.css
![alt text](<picture documents/git checkout style css.png>)


#### 12. Pulling Updates from GitHub:
If there are changes made by others in the GitHub repository, you can pull those changes into your local repository:

  ```bash
  git pull origin main
  ```
![alt text](<picture documents/git pull origin main.png>)

