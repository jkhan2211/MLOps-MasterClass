#### Testing Convention 

##### Python unittest

```
import unittest

class TestExample(unittest.TestCase):
    def test_assertion(self):
        self.assetEquals("some string", "other string")
    
    unittest.main(argv=[''], verbosity=2, exit=False)
```

#### Pytest

- all in one

Tests can be functions or class
```
def test_my_func():
    assert 1 == 1
```

Class do not need inheritance: 

```
class TestmyClass:

    def test_my_method(self):
        assert 1 == 1
```

#### Test with pytest

- create a virtual env 
```
python3 -m venv venv
source venv/bin/activate
```

install pytest
```
pip install pytest
```

Add it to requirement.txt 
