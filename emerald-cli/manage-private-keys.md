# Manage Private Keys

## Private Key Management {#private-key-management}

### Show all available accounts {#_show_all_available_accounts}

```text
$ emerald account list
```

### Exclude an account from the showing in the list {#_exclude_an_account_from_the_showing_in_the_list}

```text
$ emerald account hide  0x0e7c045110b8dbf29765047380898919c5cb56f4
```

To undo in the future:

```text
$ emerald account unhide --all
```

### Create new account {#_create_new_account}

```text
$ emerald account new \
    --security-level=high \
    --name="Test account" \
    --description="Some description" \
    < echo "secret passphrase"
```

### Show private key {#_show_private_key}

```text
$ emerald account strip 0x0e7c045110b8dbf29765047380898919c5cb56f4 < echo "secret passphrase"
```

### Change private key passphrase {#_change_private_key_passphrase}

```text
$ emerald account strip 0x0e7c045110b8dbf29765047380898919c5cb56f4 < echo "old passphrase" \
$ emerald account new --raw < echo "new passphrase"
```

### Change account name {#_change_account_name}

```text
$ emerald account update \
    0x0e7c045110b8dbf29765047380898919c5cb56f4 \
    --name="New name" \
    --description="A new description"
```

### Import keyfile {#_import_keyfile}

Import content of whole folder:

```text
$ emerald account import --all <path_to_files>
```

or single keyfile:

```text
$ emerald account import <path_to_file>
```

If keyfile already exist in a storage, import will be ignore.

To override existing Keyfile, use `-f | --force` option:

```text
$ emerald account import --force <path_to_file>
```

### Export keyfile {#_export_keyfile}

Export all keyfiles into directory:

```text
$ emerald account export --all <path_to_export_dir>
```

or single keyfile for selected &lt;address&gt;:

```text
$ emerald account export <address> <path_to_export_dir>
```

