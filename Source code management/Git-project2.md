# Hands on Lab: Using Git to track progress, manage changes for a simple form
This documentation is designed to walk you through how to use Git to track progress, manage changes, and revert project back to the previous version if needed in case of errors. To proceed with the project you will have to clone the simple-form repository using the `git clone` command.
```
git clone https://github.com/Dreyshantel/simple-form.git
```
<img width="900" height="213" alt="image" src="https://github.com/user-attachments/assets/be6aad44-5a29-4c4b-bec6-8caff8df4fc5" />


Once this is done, we will have to switch into the simple-form directory to stage the form files. Afterwards, you're going to place this client HTML Form (form.html) and CSS (style.css) form into the working directory..
```
# HTML file
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Contact Form</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<div class="container">
    <h2>Contact Us</h2>
    <form>
        <label for="name">Name</label>
        <input type="text" id="name" name="name" required>

        <label for="email">Email</label>
        <input type="email" id="email" name="email" required>

        <label for="message">Message</label>
        <textarea id="message" name="message" rows="5" required></textarea>

        <button type="submit">Submit</button>
    </form>
</div>

</body>
</html>
```

```
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

.container {
    background: #fff;
    padding: 20px;
    border-radius: 8px;
    width: 300px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

h2 {
    text-align: center;
}

label {
    display: block;
    margin-top: 10px;
}

input, textarea {
    width: 100%;
    padding: 8px;
    margin-top: 5px;
    border: 1px solid #ccc;
    border-radius: 5px;
}

button {
    margin-top: 15px;
    width: 100%;
    padding: 10px;
    background-color: #007BFF;
    color: #fff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #0056b3;
}
```

Now that we have placed the files in your working directory, you can track the current git status using `git status`, add both files to the staging area using the following command `git add form.html style.css`, and commit your initial version into your local git repository `git commit -m "message"`.
<img width="1207" height="382" alt="image" src="https://github.com/user-attachments/assets/657b98d6-9584-4769-9217-caae187714b6" />

Push the initial commit to the initial commit to the remote repository. `git push origin main"
<img width="1255" height="302" alt="image" src="https://github.com/user-attachments/assets/0056af53-79ae-4009-8dc5-23a60f0cfc7c" />

## How to make and track changes
Let's asssume your client request some new features to be added to the form. so you modify the form.html to include an additional field for phone number and add styling to the style.css file. After making these changes, stage and commit the updated files, and push them to your remote repository.
<img width="1225" height="673" alt="image" src="https://github.com/user-attachments/assets/38fb8119-0dd3-45ba-b6c0-d79190a791c3" />
<img width="1130" height="164" alt="image" src="https://github.com/user-attachments/assets/b524082b-ee5f-46a5-8d86-070eddccf008" />

After working on several features and fixes, view the git history to check all changes you have made.
<img width="1202" height="615" alt="image" src="https://github.com/user-attachments/assets/b3e8ec71-849a-4ea5-ba69-2a9c977ad224" />


## How to revert to the previous changes
Your client noticed the new changes you made introduced bugs into form submission process.you need to revert form.html file back to the last working version. First, find the commit hash of the last working version using `git log` then run `git checkout 
<img width="882" height="181" alt="image" src="https://github.com/user-attachments/assets/5558a958-582a-40c1-881b-5cba04655a8e" />

## Branching for new features
You want to experiment by adding CAPTCHA feature to the form. Create a new branch name feature-add-captcha and switch to it using: `git checkout -b feature-add-captcha`. Make the necessary changes to the file, add and commit it to the git repository. Merge the changes back to the main branch and push your new chnages to the remote repository.
<img width="1238" height="752" alt="image" src="https://github.com/user-attachments/assets/bf867eed-d457-4c3a-a1cd-264ed69a5e0d" />

## Undoing local changes
You accidentally made some unwanted changes to the style.css that you havent commited yet. Discard these local changes and revert it to the previous working file using `git checkout -- style.css`
<img width="1266" height="351" alt="image" src="https://github.com/user-attachments/assets/38853f4f-b7dd-4308-8c77-89d189b2ce96" />

**Pulling update from github**: If there are changes made by other developers on the remote repository, you can pull them to your local repository with the following command: `git pull origin main`



You can test by running a simple server so everything behaves properly. then open http://localhost:8000/form.html
```
python -m http.server 8000
```
<img width="1280" height="728" alt="image" src="https://github.com/user-attachments/assets/0f39232f-c19b-4f27-a446-6f0364794eeb" />


