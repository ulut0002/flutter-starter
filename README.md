# Flutter Boilerplate

## Overview

This is a structured Flutter boilerplate designed for scalable application development. It incorporates best practices such as clean architecture, Riverpod for state management, and modular folder organization.

## Features

- **State Management**: Uses `flutter_riverpod` for efficient state management.
- **Networking**: `dio` is used for making API calls.
- **Local Storage**: `hive` and `shared_preferences` for persistent data storage.
- **Environment Configuration**: `flutter_dotenv` for managing environment variables.
- **Image Caching**: `cached_network_image` for optimized network image loading.
- **Dependency Injection**: Clean structure with providers to facilitate DI.
- **Code Generation**: Uses `freezed` and `json_serializable` for immutable models and JSON parsing.

## Folder Structure

```
lib/
│── common/                # Shared utilities, constants, and widgets
│   ├── constants/         # Constant values
│   ├── extensions/        # Dart extensions
│   ├── utils/             # Utility functions
│   ├── widgets/           # Common reusable widgets
│
│── config/                # App configuration
│   ├── app_config.dart    # General app settings
│   ├── env.dart           # Environment-specific settings
│   ├── flavor.dart        # Different build flavors
│
│── core/providers/        # Global providers
│
│── features/feature1/     # Feature-based module structure
│   ├── data/              # Data layer
│   │   ├── data_sources/  # Local & remote data sources
│   │   ├── repositories/  # Repository implementations
│   │   ├── models/        # Data models
│   ├── domain/            # Business logic layer
│   │   ├── entities/      # Core entities
│   │   ├── repositories/  # Abstract repository contracts
│   │   ├── use_cases/     # Use case definitions
│   ├── presentation/      # UI and state management
│   │   ├── providers/     # Feature-specific providers
│   │   ├── screens/       # UI screens
│   │   ├── widgets/       # Feature-specific widgets
│
│── main.dart              # Entry point
```

## Dependencies

The following packages are used in this project:

### Main Dependencies:

```yaml
flutter_riverpod: ^2.6.1
riverpod_annotation: ^2.6.1
dio: ^5.8.0+1
shared_preferences: ^2.5.1
hive: ^2.2.3
flutter_dotenv: ^5.2.1
cached_network_image: ^3.4.1
intl: ^0.20.2
url_launcher: ^6.3.1
```

### Dev Dependencies:

```yaml
build_runner: ^2.4.14
freezed: ^2.5.8
freezed_annotation: ^2.4.4
json_serializable: ^6.9.3
riverpod_generator: ^2.6.4
riverpod_lint: ^2.6.4
custom_lint: ^0.7.2
```

## Getting Started

### 1. Install Dependencies

Run the following command to install all dependencies:

```sh
flutter pub get
```

### 2. Generate Code (if applicable)

Run the following command for code generation:

```sh
flutter pub run build_runner build --delete-conflicting-outputs
```

### 3. Configure Environment Variables

Create a `.env` file in the root directory and define necessary environment variables.

### 4. Run the Application

To run the app, use:

```sh
flutter run
```

## Contribution Guidelines

- Follow the existing folder structure for modularity.
- Use Riverpod for state management.
- Write unit tests for new features where applicable.

## License

This project is open-source under the MIT License.
