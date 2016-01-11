### Check IAM Users API Keys

This BASH script checks the age of the API keys for all your AWS IAM users.
It's good practice to rotate these keys every 60 to 90 days.

**Requirements:**

* The awscli `sudo pip install awscli`
* A valid profile in `~/.aws/config` or `${AWS_CONFIG_FILE}` with the appropriate API keys
* MacOS `date` command/format

**Usage:**

```
key-chkr.sh --profile <profile_name>
```

**Output:**

```
./key-chkr.sh --profile eng

Checking keys for user, user01...
 * Active key 1 is 368 days old
 * Active key 2 is 368 days old

Checking keys for user, user02...
 * Active key 1 is 649 days old

Checking keys for user, user03...
 * Active key 1 is 1027 days old

Checking keys for user, user04...
 * Active key 1 is 10 days old

Checking keys for user, user05...
 * Active key 1 is 12 days old

Checking keys for user, user06...
 * Active key 1 is 114 days old
 * Active key 2 is 113 days old

Checking keys for user, user07...
 * No access keys

Checking keys for user, user08...
 * Active key 1 is 485 days old

Checking keys for user, user09...
 * Active key 1 is 26 days old
 * Active key 2 is 26 days old

Checking keys for user, user10...
 * Active key 1 is 557 days old
```

**To Do:**

- [ ] Modify to handle/use the `date` command from other linux flavors
