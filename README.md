# CCTray Spec

[cctray.org](https://cctray.org/)

## Implementing

If you are building a server or client for the CCTray format, you can read about the spec at
[cctray.org](https://cctray.org/).

## Contributing

If you have created a server or client that understands the CCTray format please submit a PR to this repo to get it
added to the site.

### Prerequisites

You'll need the follow tools installed to run locally:
* [Ruby](https://www.ruby-lang.org/)

#### Ruby

[chruby](https://github.com/postmodern/chruby) and [ruby-install](https://github.com/postmodern/ruby-install) are
supported and can be used to install the correct version of Ruby.

If you choose to install Ruby manually the correct version can be found in the `.ruby-version` file.

### Developing locally

The following major technologies and libraries are used.

- [GitHub Pages with Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll)

#### Running

You can run the `develop.sh` script to automatically watch all the sources and recompile, see the script for more 
information.

```
./develop.sh
```

#### Verifying changes

Given the simple static nature of the site, no automated tests or CI have been set up. Therefore, you will need to
manually check and verify all changes.

### Tips

Most people will either be updating the `pages/clients.md` or `pages/servers.md` files to add new clients or servers
respectively.

Some things to keep in mind when updating these pages.

- Keep them in alphabetical order
- Update the `updated` attribute at the top of the file
- Follow the examples already in the file
