# Changelog
All notable changes to this project will be documented in this file.

## [Unreleased]

## [1.2.9.1] - 2023-06-22 - current
### Added
### Changed
    - Updated commons library to apply some bug fixes.
### Removed

## [1.2.9] - 2023-05-18 - 2023-06-22
### Added 
  - Added sdk version into the transaction model
### Changed 
 - Previous error handling to allow the creation of the fraud service even if the gps provider is unavailable
### Removed 

## [1.2.8] - 2023-05-12 - 2023-05-12
### Added 
  - Added come extra error handling to prevent the transaction to fail when some build step fails
### Changed 
### Removed 

## [1.2.7] - 2023-03-15 - 2023-05-12
### Added 
### Changed 
  - Changed transaction model to add information about the sim card
### Removed 

## [1.2.6] - 2023-02-02 - 2023-03-15
### Added 
### Changed 
  - Changed transaction model to add the requested permissions and if they are granted.
  - Changed transaction model to add if the gps and wifi providers are enabled.
### Removed 

## [1.2.5] - 2023-01-13 - 2023-02-02
### Added 
### Changed 
    - Fixed proguard configuration causing the consumer application to be repackaged into our library internal folder
### Removed 

## [1.2.4] - 2023-01-10 - 2023-01-13
### Added 
### Changed 
    - Errors during the send transaction callback will now be logged instead of redirected to the exception callback.
### Removed 

## [1.2.3] - 2022-12-09 - 2023-01-10
### Added 
### Changed 
    - Fixed issue with the fingerprint id.
### Removed 

## [1.2.2] - 2022-11-30 - 2022-12-09
### Added 
### Changed 
  - Fix a bug when not connected to a wifi.
  - Fix new lines on the encrypted ids.
  - Improved the emulation detection.
### Removed 
## [1.2.1] - 2022-11-22 - 2022-11-30
### Added 
### Changed 
  - Class name refactorization.
  - Changed the tags on the logs to match the refactorization.
  - Fraud constructor no longer supports a url host, it only allow to select the desired environment.
### Removed 


## [1.2.0] - 2022-10-12 - 2022-11-22
### Added 
 - Added kernel version into the device properties
 - Debug logs
### Changed 
 - Fixed bugs with the JSON sending strings instead of arrays
 - Improvement to the device id, installation id and fingerprint
 - GPS and Signal can no longer cause a blockage in the process
### Removed 
## [1.1.3] - 2022-09-30 - 2022-10-12
### Added 
### Changed 
 - Publish repository from nexus to github.
Removed 

## [1.1.2] - 2022-09-30 - 2022-10-12
### Added 
 - Compatibility for versions 5+
### Changed 
### Removed 

## [1.1.0] - 2022-09-22 - 2022-09-30
### Added 
 - LICENSE file added to the project
### Changed 
 - Refactor module name.
### Removed 

## [1.0.2] - 2022-09-10 - 2022-09-22
### Added 
Custom exceptions
### Changed 
 - Excluded callbacks and exceptions from offuscation for easier client use.
 - Changed model paramters names and structure.
### Removed 

## [1.0.1] - 2022-09-10 - 2022-09-12
### Added 
 - CI/CD to build and publish on the dev, testing and release branches.
### Changed 
 - Excluded callbacks and exceptions from offuscation for easier client use.
 - Changed model paramters names and structure.
### Removed 

## [1.0.0] - 2022-09-10
### Added 
 - Code obfuscation and gitignore extended.
### Changed 
 - Migrated code sections of the code to a common library.
 - Modified the behaviour of the GPS service.
### Removed 
