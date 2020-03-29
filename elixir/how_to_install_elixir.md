# Install Erlang and Elixir on Linux Mint 19.3

> This tutorial uses `asdf` to install erlang and elixir and assume you use zsh

## Install `asdf`

```
git clone https://github.com/asdf-vm/asdf.git ~/.asdf
cd ~/.asdf
git checkout "$(git describe --abbrev=0 --tags)"
```

## Add to zsh shell

```
echo -e "\n. $HOME/.asdf/asdf.sh" >> ~/.zshrc
```

## Add `asdf` plugins

```
asdf plugin-add erlang && asdf plugin-add elixir
```

## Install Erlang and Elixir

```
asdf install erlang 22.3 && asdf install elixir 1.10
```

Set them as the global version:

```
asdf global erlang 22.3 && asdf global elixir 1.10
```

> Verify versions before install

After this you can try: `iex` and this must happen:

```
$ iex
Erlang/OTP 22 [erts-10.7][source] [64-bit][smp:8:8] [ds:8:8:10][async-threads:1] [hipe]

Interactive Elixir (1.10.2) - press Ctrl+C to exit (type h() ENTER for help)
iex(1)>
```
