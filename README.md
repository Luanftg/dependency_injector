# Dependency Injector Package

A package created to manage instances for your application.

## Features

- [x] :star: Register an instance passing the `Type`, a `typedef InstanceCreator<T> = T Function()`, and `true` or `false` for `isSingleton` property.
*By default `isSingleton` property is set to true.*

```dart
 void register<T extends Object>(
    InstanceCreator<T> instance, {
    bool isSingleton = true,
  })
```

- [x] :star: Get an instance of a register Type.

```dart
  T get<T extends Object>()
```

- [x] :star: Callable Interface for the **get** method.

```dart
  call<T extends Object>() => get<T>();
```

## Getting started

Import the package on the `pubspec.yaml`.

```yaml
dependencies:
  dependency_injector:
    git: https://github.com/Luanftg/dependency_injector
```

## Usage

This is a simple example for the entire usage of this package.

```dart
import 'package:dependency_injector/dependency_injector_base.dart';

Future<void> main() async{
  
  final di = DependencyInjector();
  //register a Type
  di.register<DBConfiguration>(() => MySqlDBConfiguration());
  //get an instance
  final userAPi = di.get<UserApi>();
  //get from callable interface
  final userAPi = di<UserApi>();
}
```

## Additional information

<h3>Author: Luan Fonseca Torralbo Gimenez</h3>
</div>

<table align="center">

  <tr>
<td align="center">
      <a href="https://github.com/Luanftg">
        <img src="https://avatars.githubusercontent.com/u/51548623?v=4" width="100px;" alt="Foto do Luan Fonseca Torralbo Gimenez"/><br>
        <sub>
          <b>Luan F. T. Gimenez</b>
        </sub>
      </a>
    </td>
    </tr>
</table>
</div>