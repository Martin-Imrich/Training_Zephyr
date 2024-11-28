## Environment setup
Since this application uses several libraries of specific versions, usage of virtual environment is recommended. To setup venv follow instruction below. Application has been tested with python version 3.10.4.

Note: Once environment is created and all packages are installed, it is still needed to activate environment each time you open new terminal. (Tip: VScode might be configured to do it automatically.)
- Create virtual environment:
    ```
    python -m venv venv
    ```
- Activate virtual environment:
    ```
    .\venv\Scripts\activate
    ```
- Install required libraries:
    ```
    pip install -r requirements.txt
    ```
- Create UserConfig.xml with your paths. (See UserConfigTeplate.xml)

## Run application
Once environment has been setup, application might be started by following command. (Please be sure, you have activated venv in your terminal)
```
python main.py
```

## How to use
Detail explanation how to use this tool can be found in 'Doc/Frame_Selector_V2_Manual.pdf'.


