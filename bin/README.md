# Python For Steve

Showin Steve how to do some python junk.

### Required Stuff:

    * Nosetests
        - can install with 'pip install nose'
    * Doxygen
        - Can be installed with apt-get on Linux or brew on mac.

### Versioning in Git
To version this in git, first go to the github.com and create a new repository. Enter the name of the
repository (we will use PythonForSteve) and click "create repository". Do *not* select the "Initialize this repo with a README" option.
We will not need it. Then you can navigate to this directory on the command line and follow the instructions on github "...or create a new repository on the command line"
Your python code is now versioned.

## Create a gitignore
There is often files generated by running or compiling code that you do not want to have versioned (binaries, images, input files). We can instruct git to
automatically ignore these files by creating a gitignore. In your favorite editor,
make a new file called .gitignore and put the following in it:

```
*.pyc
```

This will tell git to ignore any file that ends with '.pyc'.
Now you can add this file to your repository:

```bash
git add .gitignore
git commit -m "Adding gitignore"
git push
```

Now anytime you make a change to any code, you can version it in the repo by
doing:

```bash
git commit -am "message"  #If the file is already in the repo
git add <file> ; git commit -m "message"  #If it is a new file you want to version
git push
```

### Unit Testing with Nose
To run the tests one simply needs to type:

    nosetests -v

This will produce a report on the result of the tests.
Now try changing the line int **Square.py**:

```python
    def getArea(self):
        """!Get the area of the square.

        @return The area of the square.
        """
        return self.side * self.side
```
To:
```python
    def getArea(self):
        """!Get the area of the square.

        @return The area of the square.
        """
        return self.side * 2
```
Now rerun the tests to see what happens.

### Document with doxygen

To run doxygen, first make a configuration file with:

    doxygen -g

Then you can run doxygen with:

    doxygen

This will produce a few folders. To view the documentation webpage just navigate to the html folder and open index.html.
