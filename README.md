# Welcome to pyNodeBB

pyNodeBB is a Python client for the NodeBB REST API (nodebb-plugin-write-api).

## Install

1. I'm assuming you have NodeBB installed. If not, please refer to their install guide [here](https://docs.nodebb.org/en/latest/installing/os.html).
1. NodeBB by default doesn't provide a write-api (only read). Thankfully, there's a plugin called [nodebb-plugin-write-api](https://github.com/NodeBB/nodebb-plugin-write-api) that provides some functionality for us. This plugin is required for pyNodeBB to work.
1. After you've correctly installed nodebb-plugin-write-api to your NodeBB instance, create a master token under `/admin/plugins/write-api/`.
1. Awesome. The last step is to install `pynodebb` from the CheeseShop `pip` or `easy_install`:

  ```bash
  pip install pynodebb
  ```

## Example usage

```python
from __future__ import print_function
from pynodebb import Client

client = Client('http://localhost:4567', 'master_token')
user = client.users.get(uid)

print(user['username'])
```

You can read more about their NodeBB's API endpoints [here](https://github.com/NodeBB/nodebb-plugin-write-api/blob/master/routes/v1/readme.md).

## Contribution

*todo*

## License

[MIT](https://github.com/davidvuong/pynodebb/blob/master/LICENSE.md)