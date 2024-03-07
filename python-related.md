
### Creating new project

```
mkdir project_name
cd project_name
```

create venv

```
python -m venv env
```

activate venv
navigate env --> Scripts --> Activate.ps1 --> change terminal to command prompt

or:
```
<venv_name>\Scripts\activate
```

--> requirements.txt

create requirements.txt

- directly use in folder ui or:
pip freeze > requirements.txt

- for best practice on writing the requirements refer:
https://note.nkmk.me/en/python-pip-install-requirements/#:~:text=Install%20packages%20with%20pip%3A%20%2Dr%20requirements.txt,-Use%20the%20command&text=You%20can%20name%20the%20configuration,%2Fto%2Frequirements.txt%20.

--> install related libraries
```
pip install -r requirements.txt
```

--> check libraries are installed

```
pip list
```

### Configuring logger

configure logger manually using
- handlers
- formatters

5 levels of logging
- logger.debug
- logger.info
- logger.warning
- logger.error
- logger.critical

if the logger setLevel=ERROR
only logger.error & above ie. logger.critical will be saved into the log file

quick setup
```
import logging

logger = logging.getLogger('<placeholder_logger_name>')
logger.setLevel(logging.DEBUG)
formatter = logging.Formatter('%(asctime)s - %(levelname)s - %(message)s')
file_handler = logging.FileHandler('<path_to_save_the_file>.log')
file_handler.setFormatter(formatter)
logger.addHandler(file_handler)

```

apply logger at regular places
```
logger.info('the_message %s', variable_s)
logger.error('the_error %s', variable_s)
```

Python for Leetcode

- focus on arrays & hashing
	- using set
	- using map

class Solution:

    def twoSum(self, nums: List[int], target: int) -> List[int]:

        remainder_map = dict()

        for n in range(len(nums)):


            current = nums[n]

            remainder = target - current

  
            if remainder_map.get(current) is not None:

                return [remainder_map.get(current), n]

  
            remainder_map[remainder] = n


class Solution:

    def nextGreaterElement(self, nums1: List[int], nums2: List[int]) -> List[int]:

        output = []

        nums2_dict = dict()

  

        for n in range(len(nums2)):

            nums2_dict[nums2[n]] = n

  

        for i in range(len(nums1)):

  

            index = nums2_dict.get(nums1[i])

  

            for j in range(index, len(nums2)):

                if nums2[j] > nums1[i]:

                    output.append(nums2[j])

                    break

  

                if j == len(nums2) - 1:

                    output.append(-1)

        return output