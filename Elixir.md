# Elixir

<img src="https://elixir-lang.org/images/logo/logo.png" style="height: 64px;">

[Elixir](https://elixir-lang.org/) is a functional (more like [/FP]()-first for me) language running on the [BEAM](https://en.wikipedia.org/wiki/BEAM_(Erlang_virtual_machine)) ([Erlang](https://en.wikipedia.org/wiki/Erlang_(programming_language))'s VM). One may think about Elixir as "Ruby on BEAM" especially if one knows about the [Phoenix framework](https://www.phoenixframework.org/). The language itself is dynamically typed but there is an opportunity for static analysis using Erlang's [dialyzer](https://erlang.org/doc/man/dialyzer.html) through [dialyxir](https://github.com/jeremyjh/dialyxir).

# Resources

- [Hex.pm](https://hex.pm/), a package repository for Erlang/Elixir

# How to

I ([/who/astynax]()) install Erlang & Elixir with [/asdf]():

1. Erlang

    ```shell
    $ asdf plugin-add erlang
    $ asdf plugin-add elixir
    $ asdf install erlang 23.2.1
    $ asdf global erlang 23.2.1
    ```

2. Elixir itself
  
    ```shell
    $ # this may speed the installation up
    $ export KERL_CONFIGURE_OPTIONS="--disable-debug --without-javac"
    $ asdf install elixir 1.11.3-otp-23
    $ asdf global elixir 1.11.3-otp-23
    ```
```

Here `otp-23` means what you want to install Elixir with the support of [OTP](https://en.wikipedia.org/wiki/Open_Telecom_Platform) v23 (see `erlang 23.2.1` above).