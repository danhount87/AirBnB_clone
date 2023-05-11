# 0x00. AirBnB clone - The console

## Concepts
For this project, we expect you to look at these concepts:

<a href="/concepts/66">Python packages</a>
<a href="/concepts/74">AirBnB clone</a>


<img src="https://s3.amazonaws.com/alx-intranet.hbtn.io/uploads/medias/2018/6/65f4a1dd9c51265f49d0.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=AKIARDDGGGOUSBVO6H7D%2F20230511%2Fus-east-1%2Fs3%2Faws4_request&amp;X-Amz-Date=20230511T162141Z&amp;X-Amz-Expires=86400&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Signature=d84a1c338680c7baedf5bdc30d7b4bb48d1a3201969e3ac07d1e0caea3318a0f" alt="" loading="lazy" style="">


Background Context
Welcome to the AirBnB clone project!

Before starting, please read the AirBnB concept page.
First step: Write a command interpreter to manage your AirBnB objects.

This is the first step towards building your first full web application: the AirBnB clone. This first step is very important because you will use what you build during this project with all other following projects: HTML/CSS templating, database storage, API, front-end integration…

Each task is linked and will help you to:

    put in place a parent class (called BaseModel) to take care of the initialization, serialization and deserialization of your future instances
    create a simple flow of serialization/deserialization: Instance <-> Dictionary <-> JSON string <-> file
    create all classes used for AirBnB (User, State, City, Place…) that inherit from BaseModel
    create the first abstracted storage engine of the project: File storage.
    create all unittests to validate all our classes and storage engine

What’s a command interpreter?

Do you remember the Shell? It’s exactly the same but limited to a specific use-case. In our case, we want to be able to manage the objects of our project:

    Create a new object (ex: a new User or a new Place)
    Retrieve an object from a file, a database etc…
    Do operations on objects (count, compute stats, etc…)
    Update attributes of an object
    Destroy an object

# Resources

Read or watch:

    <a href="/rltoken/8ecCwE6veBmm3Nppw4hz5A" title="cmd module" target="_blank">cmd module</a>
    <a href="/rltoken/uEy4RftSdKypoig9NFTvCg" title="cmd module in depth" target="_blank">cmd module in depth</a>
    packages concept page
    <a href="/rltoken/KfL9TqwdI69W6ttG6gTPPQ" title="uuid module" target="_blank">uuid module</a>
    <a href="/rltoken/1d8I3jSKgnYAtA1IZfEDpA" title="datetime" target="_blank">datetime</a>
    <a href="/rltoken/IlFiMB8UmqBG2CxA0AD3jA" title="unittest module" target="_blank">unittest module</a>
    <a href="/rltoken/C_a0EKbtvKdMcwIAuSIZng" title="args/kwargs" target="_blank">args/kwargs</a>
    <a href="/rltoken/tgNVrKKzlWgS4dfl3mQklw" title="Python test cheatsheet" target="_blank">Python test cheatsheet</a>
    <a href="/rltoken/EvcaH9uTLlauxuw03WnkOQ" title="cmd module wiki page" target="_blank">cmd module wiki page</a>
    <a href="/rltoken/begh14KQA-3ov29KvD_HvA" title="python unittest" target="_blank">python unittest</a>

# Learning Objectives

At the end of this project, you are expected to be able to explain to anyone, without the help of Google:
## General

    How to create a Python package
    How to create a command interpreter in Python using the cmd module
    What is Unit testing and how to implement it in a large project
    How to serialize and deserialize a Class
    How to write and read a JSON file
    How to manage datetime
    What is an UUID
    What is *args and how to use it
    What is **kwargs and how to use it
    How to handle named arguments in a function

# Requirements
## Python Scripts

    Allowed editors: vi, vim, emacs
    All your files will be interpreted/compiled on Ubuntu 20.04 LTS using python3 (version 3.8.5)
    All your files should end with a new line
    The first line of all your files should be exactly #!/usr/bin/python3
    A README.md file, at the root of the folder of the project, is mandatory
    Your code should use the pycodestyle (version 2.8.*)
    All your files must be executable
    The length of your files will be tested using wc
    All your modules should have a documentation (python3 -c 'print(__import__("my_module").__doc__)')
    All your classes should have a documentation (python3 -c 'print(__import__("my_module").MyClass.__doc__)')
    All your functions (inside and outside a class) should have a documentation (python3 -c 'print(__import__("my_module").my_function.__doc__)' and python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)')
    A documentation is not a simple word, it’s a real sentence explaining what’s the purpose of the module, class or method (the length of it will be verified)

## Python Unit Tests

    Allowed editors: vi, vim, emacs
    All your files should end with a new line
    All your test files should be inside a folder tests
    You have to use the unittest module
    All your test files should be python files (extension: .py)
    All your test files and folders should start by test_
    Your file organization in the tests folder should be the same as your project
    e.g., For models/base_model.py, unit tests must be in: tests/test_models/test_base_model.py
    e.g., For models/user.py, unit tests must be in: tests/test_models/test_user.py
    All your tests should be executed by using this command: python3 -m unittest discover tests
    You can also test file by file by using this command: python3 -m unittest tests/test_models/test_base_model.py
    All your modules should have a documentation (python3 -c 'print(__import__("my_module").__doc__)')
    All your classes should have a documentation (python3 -c 'print(__import__("my_module").MyClass.__doc__)')
    All your functions (inside and outside a class) should have a documentation (python3 -c 'print(__import__("my_module").my_function.__doc__)' and python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)')
    We strongly encourage you to work together on test cases, so that you don’t miss any edge case


# More Info

## Execution
Your shell should work like this in interactive mode:

$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb) 
(hbnb) 
(hbnb) quit
$

But also in non-interactive mode: (like the Shell project in C)

$ echo "help" | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 
$
$ cat test_help
help
$
$ cat test_help | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 
$


All tests should also pass in non-interactive mode: $ echo "python3 -m unittest discover tests" | bash

<img src="https://s3.amazonaws.com/alx-intranet.hbtn.io/uploads/medias/2018/6/815046647d23428a14ca.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=AKIARDDGGGOUSBVO6H7D%2F20230511%2Fus-east-1%2Fs3%2Faws4_request&amp;X-Amz-Date=20230511T162141Z&amp;X-Amz-Expires=86400&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Signature=390a9589c7e211db8509722f56c8e74808d26691018ccf93c7d3af54e0e5a101" alt="" loading="lazy" style="">


<div><div class="panel panel-default sm-gap"><div class="panel-heading panel-heading-actions"><h3 class="panel-title">Video library<small style="margin-left: 8px;">(8 total)</small></h3></div><div class="list-group"><div class="list-group-item"><div class="align-items-center d-flex" style="position: relative; width: 100%;"><input class="form-control" placeholder="Search by title" type="search" value=""></div></div></div><div class="list-group"><div style="display: flex; flex-flow: row wrap;"><span data-container="body" data-html="false" data-placement="auto top" data-toggle="tooltip" title="" data-original-title="HBNB project overview of each part"><div style="cursor: pointer; display: flex; flex-direction: column; margin: 10px;"><div style="position: relative;"><div style="background-color: rgb(0, 0, 0); background-image: url(&quot;https://hbtn-vod-input-prod.s3-accelerate.amazonaws.com/ALX/16966eb2f1a059c5e0282d5588288e5729446ea17fbf4e1f4fca0867d788f812/16966eb2f1a059c5e0282d5588288e5729446ea17fbf4e1f4fca0867d788f812.jpg?response-content-disposition=attachment%3B&amp;X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=AKIARDDGGGOUSBVO6H7D%2F20230511%2Fus-east-1%2Fs3%2Faws4_request&amp;X-Amz-Date=20230511T162141Z&amp;X-Amz-Expires=14400&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Signature=a950321196200e3d6962669082af7c0dd9e9297478c3b989fba0b810ee8f2eac&quot;); background-position: center center; background-repeat: no-repeat; background-size: contain; border-radius: 3px; height: 126px; width: 224px;"></div></div><div style="-moz-box-orient: vertical; -webkit-line-clamp: 2; display: -webkit-box; font-size: 1.4rem; font-weight: bold; line-height: 2rem; margin-top: 6px; max-height: 4rem; max-width: 192px; overflow: hidden; padding: 0px 4px; text-overflow: ellipsis; white-space: normal;">HBNB project overview</div></div></span><span data-container="body" data-html="false" data-placement="auto top" data-toggle="tooltip" title="" data-original-title="The console part of the AirBnB clone project"><div style="cursor: pointer; display: flex; flex-direction: column; margin: 10px;"><div style="position: relative;"><div style="background-color: rgb(0, 0, 0); background-image: url(&quot;https://hbtn-vod-input-prod.s3-accelerate.amazonaws.com/ALX/116354b1cc94450120edeb9156af51725f4e0b0d18c43030c626810f8ee3fb7b/116354b1cc94450120edeb9156af51725f4e0b0d18c43030c626810f8ee3fb7b.jpg?response-content-disposition=attachment%3B&amp;X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=AKIARDDGGGOUSBVO6H7D%2F20230511%2Fus-east-1%2Fs3%2Faws4_request&amp;X-Amz-Date=20230511T162141Z&amp;X-Amz-Expires=14400&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Signature=b1ba3aa718af8963be08a9a99e1c45517798f28541fcf60d4d57fd9577f2b857&quot;); background-position: center center; background-repeat: no-repeat; background-size: contain; border-radius: 3px; height: 126px; width: 224px;"></div></div><div style="-moz-box-orient: vertical; -webkit-line-clamp: 2; display: -webkit-box; font-size: 1.4rem; font-weight: bold; line-height: 2rem; margin-top: 6px; max-height: 4rem; max-width: 192px; overflow: hidden; padding: 0px 4px; text-overflow: ellipsis; white-space: normal;">HBNB - the console</div></div></span><span data-container="body" data-html="false" data-placement="auto top" data-toggle="tooltip" title="" data-original-title="Usage of UUID in Python"><div style="cursor: pointer; display: flex; flex-direction: column; margin: 10px;"><div style="position: relative;"><div style="background-color: rgb(0, 0, 0); background-image: url(&quot;https://hbtn-vod-input-prod.s3-accelerate.amazonaws.com/ALX/738d8f17874d91803de2e5c4f9ee5a20cb872390744505627d692bbb3945b652/738d8f17874d91803de2e5c4f9ee5a20cb872390744505627d692bbb3945b652.jpg?response-content-disposition=attachment%3B&amp;X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=AKIARDDGGGOUSBVO6H7D%2F20230511%2Fus-east-1%2Fs3%2Faws4_request&amp;X-Amz-Date=20230511T162141Z&amp;X-Amz-Expires=14400&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Signature=10264b8ad255763801d669380a793439ea5011e4298265d0096389e93cc25fbd&quot;); background-position: center center; background-repeat: no-repeat; background-size: contain; border-radius: 3px; height: 126px; width: 224px;"></div></div><div style="-moz-box-orient: vertical; -webkit-line-clamp: 2; display: -webkit-box; font-size: 1.4rem; font-weight: bold; line-height: 2rem; margin-top: 6px; max-height: 4rem; max-width: 192px; overflow: hidden; padding: 0px 4px; text-overflow: ellipsis; white-space: normal;">Python: Unique Identifier</div></div></span><span data-container="body" data-html="false" data-placement="auto top" data-toggle="tooltip" title="" data-original-title="How to create and design Python Unittests"><div style="cursor: pointer; display: flex; flex-direction: column; margin: 10px;"><div style="position: relative;"><div style="background-color: rgb(0, 0, 0); background-image: url(&quot;https://hbtn-vod-input-prod.s3-accelerate.amazonaws.com/ALX/d9d017dfd1b9697b7f3d75af85aa7e2fec0397a04541a918fdc53f7a0513b21f/d9d017dfd1b9697b7f3d75af85aa7e2fec0397a04541a918fdc53f7a0513b21f.jpg?response-content-disposition=attachment%3B&amp;X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=AKIARDDGGGOUSBVO6H7D%2F20230511%2Fus-east-1%2Fs3%2Faws4_request&amp;X-Amz-Date=20230511T162141Z&amp;X-Amz-Expires=14400&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Signature=e2c5aeddd773bf9d6d767a76330c388d59c0626a4980c3451bfb049b4b85724c&quot;); background-position: center center; background-repeat: no-repeat; background-size: contain; border-radius: 3px; height: 126px; width: 224px;"></div></div><div style="-moz-box-orient: vertical; -webkit-line-clamp: 2; display: -webkit-box; font-size: 1.4rem; font-weight: bold; line-height: 2rem; margin-top: 6px; max-height: 4rem; max-width: 192px; overflow: hidden; padding: 0px 4px; text-overflow: ellipsis; white-space: normal;">Python: Unittests</div></div></span><span data-container="body" data-html="false" data-placement="auto top" data-toggle="tooltip" title="" data-original-title="Python class, base model and inheritance in the AirBnB clone project"><div style="cursor: pointer; display: flex; flex-direction: column; margin: 10px;"><div style="position: relative;"><div style="background-color: rgb(0, 0, 0); background-image: url(&quot;https://hbtn-vod-input-prod.s3-accelerate.amazonaws.com/ALX/4c8cf8b97eab59676c4330f8308a59b479978cbac4cb58928c8683129e62161b/4c8cf8b97eab59676c4330f8308a59b479978cbac4cb58928c8683129e62161b.jpg?response-content-disposition=attachment%3B&amp;X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=AKIARDDGGGOUSBVO6H7D%2F20230511%2Fus-east-1%2Fs3%2Faws4_request&amp;X-Amz-Date=20230511T162141Z&amp;X-Amz-Expires=14400&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Signature=b0a2d78fbf93dacf21f75a0cac7f67c503c9cd61ba3bf1276a7f098ac3dc49fc&quot;); background-position: center center; background-repeat: no-repeat; background-size: contain; border-radius: 3px; height: 126px; width: 224px;"></div></div><div style="-moz-box-orient: vertical; -webkit-line-clamp: 2; display: -webkit-box; font-size: 1.4rem; font-weight: bold; line-height: 2rem; margin-top: 6px; max-height: 4rem; max-width: 192px; overflow: hidden; padding: 0px 4px; text-overflow: ellipsis; white-space: normal;">Python: BaseModel and inheritance</div></div></span><span data-container="body" data-html="false" data-placement="auto top" data-toggle="tooltip" title="" data-original-title="Git usage and code consistency for better team work"><div style="cursor: pointer; display: flex; flex-direction: column; margin: 10px;"><div style="position: relative;"><div style="background-color: rgb(0, 0, 0); background-image: url(&quot;https://hbtn-vod-input-prod.s3-accelerate.amazonaws.com/ALX/a1621a12e252129ffa245698e37e5828b5a0118cc0a426db11fad50c74064e3a/a1621a12e252129ffa245698e37e5828b5a0118cc0a426db11fad50c74064e3a.jpg?response-content-disposition=attachment%3B&amp;X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=AKIARDDGGGOUSBVO6H7D%2F20230511%2Fus-east-1%2Fs3%2Faws4_request&amp;X-Amz-Date=20230511T162141Z&amp;X-Amz-Expires=14400&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Signature=b911fdae825aaa5651c444a5b4668d766b5b7a784e529057e02a54d37b35a0ea&quot;); background-position: center center; background-repeat: no-repeat; background-size: contain; border-radius: 3px; height: 126px; width: 224px;"></div></div><div style="-moz-box-orient: vertical; -webkit-line-clamp: 2; display: -webkit-box; font-size: 1.4rem; font-weight: bold; line-height: 2rem; margin-top: 6px; max-height: 4rem; max-width: 192px; overflow: hidden; padding: 0px 4px; text-overflow: ellipsis; white-space: normal;">Code consistency</div></div></span><span data-container="body" data-html="false" data-placement="auto top" data-toggle="tooltip" title="" data-original-title="Creation and usage of Python modules and packages"><div style="cursor: pointer; display: flex; flex-direction: column; margin: 10px;"><div style="position: relative;"><div style="background-color: rgb(0, 0, 0); background-image: url(&quot;https://hbtn-vod-input-prod.s3-accelerate.amazonaws.com/ALX/da9dd761329eb52dbff900227e4d05041f0a62801110942e655fb7d7b3599a0c/da9dd761329eb52dbff900227e4d05041f0a62801110942e655fb7d7b3599a0c.jpg?response-content-disposition=attachment%3B&amp;X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=AKIARDDGGGOUSBVO6H7D%2F20230511%2Fus-east-1%2Fs3%2Faws4_request&amp;X-Amz-Date=20230511T162141Z&amp;X-Amz-Expires=14400&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Signature=1dc5afd2c83c0ce7c8839823bb87d01867d2e05e3cf37d8d8c4a47e58a66a8fe&quot;); background-position: center center; background-repeat: no-repeat; background-size: contain; border-radius: 3px; height: 126px; width: 224px;"></div></div><div style="-moz-box-orient: vertical; -webkit-line-clamp: 2; display: -webkit-box; font-size: 1.4rem; font-weight: bold; line-height: 2rem; margin-top: 6px; max-height: 4rem; max-width: 192px; overflow: hidden; padding: 0px 4px; text-overflow: ellipsis; white-space: normal;">Python: Modules and Packages</div></div></span><span data-container="body" data-html="false" data-placement="auto top" data-toggle="tooltip" title="" data-original-title="How in the AirBnB clone project storage is managed"><div style="cursor: pointer; display: flex; flex-direction: column; margin: 10px;"><div style="position: relative;"><div style="background-color: rgb(0, 0, 0); background-image: url(&quot;https://hbtn-vod-input-prod.s3-accelerate.amazonaws.com/ALX/b24d6365d9d5dcecfa1e2a854ccdb533d8e5ba4bb10db0bb6c192993f53b6cfd/b24d6365d9d5dcecfa1e2a854ccdb533d8e5ba4bb10db0bb6c192993f53b6cfd.jpg?response-content-disposition=attachment%3B&amp;X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=AKIARDDGGGOUSBVO6H7D%2F20230511%2Fus-east-1%2Fs3%2Faws4_request&amp;X-Amz-Date=20230511T162141Z&amp;X-Amz-Expires=14400&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Signature=3632fb38f69ed129cd00a98538779c03484953858af038d7c0c9ba1dad4013c9&quot;); background-position: center center; background-repeat: no-repeat; background-size: contain; border-radius: 3px; height: 126px; width: 224px;"></div></div><div style="-moz-box-orient: vertical; -webkit-line-clamp: 2; display: -webkit-box; font-size: 1.4rem; font-weight: bold; line-height: 2rem; margin-top: 6px; max-height: 4rem; max-width: 192px; overflow: hidden; padding: 0px 4px; text-overflow: ellipsis; white-space: normal;">HBNB - storage abstraction</div></div></span></div></div></div></div>

