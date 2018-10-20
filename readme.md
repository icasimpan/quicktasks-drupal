*What is this*

Is my personal notes on Drupal, written using with the help of hugo.

*Adding Blog Post*
1. Make sure you have hugo installed, refer to https://gohugo.io/getting-started/installing/
2. Clone the Project
```
git clone https://github.com/icasimpan/quicktasks-drupal.git
```
3. Add a new article to your blog
```
hugo new posts/your-new-blog-post.md
```
4. Edit your post
5. Commit changes to git
```
git commit "My new awesome post!"
```


*Publish*

1. Clone the raw blog
```
git clone https://github.com/icasimpan/quicktasks-drupal.git
```
2. Go inside it
```
cd quicktasks-drupal
```
3. Get the current "public" from "gh-pages" branch:
```
git clone --branch gh-pages https://github.com/icasimpan/quicktasks-drupal.git public
```
4. Regenerate
```
hugo
```
5. Commit changes to git
```
cd public
git commit "blogpost update"
```

Hugo verion tested: v0.49.2 

Theme version used: https://github.com/arjunkrishnababu96/basics - 93d2a49
