# hello-spin
Getting started with spin https://spin.fermyon.dev

## 1. Install `spin` binary

```
git clone https://github.com/fermyon/spin
cd spin && make build
./target/release/spin --help
```

Create zsh/bash alias to use `spin` command from any directory.

Update `PATH` in ~/.zshrc` file:

```
export PATH="$PATH:/your-spin-folder/spin/target/release"
```

and now you ca run `spin` command from any directory.

```
spin --help
```

## 2. Create spin application.
First, we need to install spin template from spin repository

```
spin templates install --git https://github.com/fermyon/spin
```

To verify that we install templates successful.

```
spin templates list
```

Now, we create spin app with `http-rust` template

```
spin new http-rust
```

Build with `spin`

```
spin build
```

Running an application:

```
spin up
```

You can custom port for example start with port `5000` :

```
spin up --listen 127.0.0.1:5000
```

Done! http://localhost:5000/hello

