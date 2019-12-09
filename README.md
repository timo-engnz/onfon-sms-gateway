# Getting started

Send SMS with Onfon Media SMS Platform.

## How to Build


You must have Python ```2 >=2.7.9``` or Python ```3 >=3.4``` installed on your system to install and run this SDK. This SDK package depends on other Python packages like nose, jsonpickle etc. 
These dependencies are defined in the ```requirements.txt``` file that comes with the SDK.
To resolve these dependencies, you can use the PIP Dependency manager. Install it by following steps at [https://pip.pypa.io/en/stable/installing/](https://pip.pypa.io/en/stable/installing/).

Python and PIP executables should be defined in your PATH. Open command prompt and type ```pip --version```.
This should display the version of the PIP Dependency Manager installed if your installation was successful and the paths are properly defined.

* Using command line, navigate to the directory containing the generated files (including ```requirements.txt```) for the SDK.
* Run the command ```pip install -r requirements.txt```. This should install all the required dependencies.

![Building SDK - Step 1](https://apidocs.io/illustration/python?step=installDependencies&workspaceFolder=OnfonMedia%20SMS%20Gateway-Python)


## How to Use

The following section explains how to use the Onfonmediasmsgateway SDK package in a new project.

### 1. Open Project in an IDE

Open up a Python IDE like PyCharm. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

![Open project in PyCharm - Step 1](https://apidocs.io/illustration/python?step=pyCharm)

Click on ```Open``` in PyCharm to browse to your generated SDK directory and then click ```OK```.

![Open project in PyCharm - Step 2](https://apidocs.io/illustration/python?step=openProject0&workspaceFolder=OnfonMedia%20SMS%20Gateway-Python)     

The project files will be displayed in the side bar as follows:

![Open project in PyCharm - Step 3](https://apidocs.io/illustration/python?step=openProject1&workspaceFolder=OnfonMedia%20SMS%20Gateway-Python&projectName=onfonmediasmsgateway)     

### 2. Add a new Test Project

Create a new directory by right clicking on the solution name as shown below:

![Add a new project in PyCharm - Step 1](https://apidocs.io/illustration/python?step=createDirectory&workspaceFolder=OnfonMedia%20SMS%20Gateway-Python&projectName=onfonmediasmsgateway)

Name the directory as "test"

![Add a new project in PyCharm - Step 2](https://apidocs.io/illustration/python?step=nameDirectory)
   
Add a python file to this project with the name "testsdk"

![Add a new project in PyCharm - Step 3](https://apidocs.io/illustration/python?step=createFile&workspaceFolder=OnfonMedia%20SMS%20Gateway-Python&projectName=onfonmediasmsgateway)

Name it "testsdk"

![Add a new project in PyCharm - Step 4](https://apidocs.io/illustration/python?step=nameFile)

In your python file you will be required to import the generated python library using the following code lines

```Python
from onfonmediasmsgateway.onfonmediasmsgateway_client import OnfonmediasmsgatewayClient
```

![Add a new project in PyCharm - Step 4](https://apidocs.io/illustration/python?step=projectFiles&workspaceFolder=OnfonMedia%20SMS%20Gateway-Python&libraryName=onfonmediasmsgateway.onfonmediasmsgateway_client&projectName=onfonmediasmsgateway&className=OnfonmediasmsgatewayClient)

After this you can write code to instantiate an API client object, get a controller object and  make API calls. Sample code is given in the subsequent sections.

### 3. Run the Test Project

To run the file within your test project, right click on your Python file inside your Test project and click on ```Run```

![Run Test Project - Step 1](https://apidocs.io/illustration/python?step=runProject&workspaceFolder=OnfonMedia%20SMS%20Gateway-Python&libraryName=onfonmediasmsgateway.onfonmediasmsgateway_client&projectName=onfonmediasmsgateway&className=OnfonmediasmsgatewayClient)


## How to Test

You can test the generated SDK and the server with automatically generated test
cases. unittest is used as the testing framework and nose is used as the test
runner. You can run the tests as follows:

  1. From terminal/cmd navigate to the root directory of the SDK.
  2. Invoke ```pip install -r test-requirements.txt```
  3. Invoke ```nosetests```

## Initialization

### Authentication
In order to setup authentication and initialization of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| apikey | Transport Layer ApiKey |
| api_key | Message Layer ApiKey used for authentication purpose and pass this parameter in URL encoded format. |
| client_id | Message Layer ClientId used for authentication purpose and pass this parameter in URL encoded format. |



API client can be initialized as following.

```python
# Configuration parameters and credentials
apikey = 'TRANSPORT_LAYER_APIKEY' # Transport Layer ApiKey
api_key = 'MESSAGE_LAYER_APIKEY' # Message Layer ApiKey used for authentication purpose and pass this parameter in URL encoded format.
client_id = 'MESSAGE_LAYER_APIKEY' # Message Layer ClientId used for authentication purpose and pass this parameter in URL encoded format.

client = OnfonmediasmsgatewayClient(apikey, api_key, client_id)
```



# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [AccountController](#account_controller)
* [TemplateController](#template_controller)

## <a name="account_controller"></a>![Class: ](https://apidocs.io/img/class.png ".AccountController") AccountController

### Get controller instance

An instance of the ``` AccountController ``` class can be accessed from the API Client.

```python
 account_controller = client.account
```

### <a name="get_credit_balance"></a>![Method: ](https://apidocs.io/img/method.png ".AccountController.get_credit_balance") get_credit_balance

> Get Credit Balance

```python
def get_credit_balance(self)
```

#### Example Usage

```python

result = account_controller.get_credit_balance()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="template_controller"></a>![Class: ](https://apidocs.io/img/class.png ".TemplateController") TemplateController

### Get controller instance

An instance of the ``` TemplateController ``` class can be accessed from the API Client.

```python
 template_controller = client.template
```

### <a name="get_template_list"></a>![Method: ](https://apidocs.io/img/method.png ".TemplateController.get_template_list") get_template_list

> Get Template List

```python
def get_template_list(self)
```

#### Example Usage

```python

result = template_controller.get_template_list()

```


### <a name="create_new_template"></a>![Method: ](https://apidocs.io/img/method.png ".TemplateController.create_new_template") create_new_template

> Create New Template

```python
def create_new_template(self,
                            message_template,
                            template_name)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| messageTemplate |  ``` Required ```  | Template text. |
| templateName |  ``` Required ```  | Name of template |



#### Example Usage

```python
message_template = 'MessageTemplate'
template_name = 'TemplateName'

result = template_controller.create_new_template(message_template, template_name)

```


[Back to List of Controllers](#list_of_controllers)



