## README

This is your {{cookiecutter.folder_name}} directory 

## Getting started with vscode 

* Make sure `Docker` is running 
* Open `user settings`, in mac `cmd` + `shift` + `p`. 
    * Select `Remote-containers: Open folder in container` 
* Wait for it to build
* Done! 


## Using terminal

Make sure `make` is installed then:

* `make build` 
* `make bash` 

### Launching Jupyter notebook

You can launch the notebook from bash with this command:

```bash
jupyter notebook --ip 0.0.0.0 --port 8888 --no-browser --allow-root
```

Or you can add it in dockerfile in the last line:

```Dockerfile
CMD jupyter notebook --ip 0.0.0.0 --port 8888 --no-browser --allow-root
```

and run docker with `make notebook`. 

### Launching Jupyter Lab

Similarily, run jupyter lab after `make bash`: 

```bash
jupyter lab --ip 0.0.0.0 --port 8888 --no-browser --allow-root
```