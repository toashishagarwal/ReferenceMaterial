# Virtual Env Management using PIP

Command | Windows 11  | Mac |
--- | --- | --- |
Create a python virtual env called venv | python -m venv venv | python3 -m venv venv |
Activate the virtual env  | .\venv\Scripts\Activate.ps1 | source venv/bin/activate |
Install the dependencies | pip install -r requirements.txt | pip install -r requirements.txt |
Deactivate the virtual env | deactivate |deactivate|


NOTE: If you get permission error while activating virtual env on windows, you may have to run the below command
```bash
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

# As individual sections
## Steps to create & activate virtual env (for Windows 11)
### 1. Create a python virtual env called venv
```bash
python -m venv venv
```

### 2. Activate the virtual env
```bash
.\venv\Scripts\Activate.ps1
```

(If you get permission error, you may have to run the below command)
```bash
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

### 3. Install the dependencies
```bash
pip install -r requirements.txt
```

## 4. Deactivate the virtual env
```bash
deactivate
```

## Steps to create & activate virtual env (for MAC)

### 1. Create a python virtual env called venv
```bash
python3 -m venv venv
```

### 2. Activate the virtual env 
```bash
source venv/bin/activate
```

### 3. Install the dependencies
```bash
pip install -r requirements.txt
```
## 4. Deactivate the virtual env
```bash
deactivate
```
