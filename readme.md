Repository to reproduce a possible dedupe regression between 0.27.0 and 0.27.1

**Edit: This was not a bug, pickadate should be using `peerDependencies` for jquery, not `dependencies`**

# 0.27.0

```
~/Desktop/testing-yarn $ ./yarn-0.27.0/node_modules/.bin/yarn install
yarn install v0.27.0
info No lockfile found.
[1/4] Resolving packages...
[2/4] Fetching packages...
0/2[3/4] Linking dependencies...
0/2 0/247 155/247 0/4[4/4] Building fresh packages...
success Saved lockfile.
Done in 1.25s.
```

## yarn.lock

```
# THIS IS AN AUTOGENERATED FILE. DO NOT EDIT THIS FILE DIRECTLY.
# yarn lockfile v1


jquery@>=1.7, jquery@^2.1.3:
  version "2.2.4"
  resolved "https://registry.yarnpkg.com/jquery/-/jquery-2.2.4.tgz#2c89d6889b5eac522a7eea32c14521559c6cbf02"

pickadate@^3.5.6:
  version "3.5.6"
  resolved "https://registry.yarnpkg.com/pickadate/-/pickadate-3.5.6.tgz#c998302343b79a19954fc49c45cc708347602806"
  dependencies:
    jquery ">=1.7"
```

# 0.27.1

```
~/Desktop/testing-yarn $ ./yarn-0.27.1/node_modules/.bin/yarn install
yarn install v0.27.1
info No lockfile found.
[1/4] Resolving packages...
[2/4] Fetching packages...
0/3[3/4] Linking dependencies...
0/3 0/366 169/366 0/5[4/4] Building fresh packages...
success Saved lockfile.
Done in 0.92s.
```

## yarn.lock

```
# THIS IS AN AUTOGENERATED FILE. DO NOT EDIT THIS FILE DIRECTLY.
# yarn lockfile v1


jquery@>=1.7:
  version "3.2.1"
  resolved "https://registry.yarnpkg.com/jquery/-/jquery-3.2.1.tgz#5c4d9de652af6cd0a770154a631bba12b015c787"

jquery@^2.1.3:
  version "2.2.4"
  resolved "https://registry.yarnpkg.com/jquery/-/jquery-2.2.4.tgz#2c89d6889b5eac522a7eea32c14521559c6cbf02"

pickadate@^3.5.6:
  version "3.5.6"
  resolved "https://registry.yarnpkg.com/pickadate/-/pickadate-3.5.6.tgz#c998302343b79a19954fc49c45cc708347602806"
  dependencies:
    jquery ">=1.7"
```

# 0.27.5

```
~/Desktop/testing-yarn $ ./yarn-0.27.5/node_modules/.bin/yarn install
yarn install v0.27.5
info No lockfile found.
[1/4] Resolving packages...
[2/4] Fetching packages...
0/3[3/4] Linking dependencies...
0/3 0/119 0/5[4/4] Building fresh packages...
success Saved lockfile.
Done in 0.88s.
```

## yarn.lock

```
# THIS IS AN AUTOGENERATED FILE. DO NOT EDIT THIS FILE DIRECTLY.
# yarn lockfile v1


jquery@>=1.7:
version "3.2.1"
resolved "https://registry.yarnpkg.com/jquery/-/jquery-3.2.1.tgz#5c4d9de652af6cd0a770154a631bba12b015c787"

jquery@^2.1.3:
version "2.2.4"
resolved "https://registry.yarnpkg.com/jquery/-/jquery-2.2.4.tgz#2c89d6889b5eac522a7eea32c14521559c6cbf02"

pickadate@^3.5.6:
version "3.5.6"
resolved "https://registry.yarnpkg.com/pickadate/-/pickadate-3.5.6.tgz#c998302343b79a19954fc49c45cc708347602806"
dependencies:
jquery ">=1.7"
```
