# Release Notes

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html)
from version 0.14.0.

## Unreleased

### Added

* LOGIQ Backend (logiq)

### Fixed

* Splunx XML rule name is now set to rule title

## 0.16.0 - 2020-02-25

### Added

* Proxy field names to ECS mapping (ecs-proxy) configuration
* False positives metadata to LimaCharlie backend
* Additional aggregation capabilitied for es-dsl backend.
* Azure log analytics rule backend (ala-rule)
* SQL backend
* Splunk Zeek sourcetype mapping config
* sigma2attack script
* Carbon Black backend and configuration
* ArcSight ESM backend
* Elasticsearch detection rule backend

### Changed

* Kibana object id is now Sigma rule id if available. Else
  the old naming scheme is used.
* sigma2misp: replacement of deprecated method usage.
* Various configuration updates
* Extended ArcSight mapping

### Fixed

* Fixed aggregation queries for Elastalert backend
* Fixed aggregation queries for es-dsl backend
* Backend and configuration lists are sorted.
* Escaping in ala backend

## 0.15.0 - 2019-12-06

### Added

* sigma-uuid tool for addition and check of Sigma rule identifiers
* Default configurations
* Restriction of compared rules in sigma-similarity
* Regular expression support in es-dsl backend
* LimaCharlie support for proxy rule category
* Source distribution for PyPI

### Changed

* Type errors are now ignored with -I

### Fixed

* Removed wrong mapping of CommandLine field mapping in THOR config

## 0.14 - 2019-11-10

### Added

* sigma-similarity tool
* LimaCharlie backend
* Default configurations for some backends that are used if no configuration is passed.
* Regular expression support for es-dsl backend (propagates to backends derived from this like elastalert-dsl)
* Value modifiers:
    * startswith
    * endswith

### Changed

* Removal of line breaks in elastalert output
* Searches not bound to fields are restricted to keyword fields in es-qs backend
* Graylog backend now based on es-qs backend

### Fixed

* Removed ProcessCommandLine mapping for Windows Security EventID 4688 in generic
  process creation log source configuration.

## 0.13 - 2019-10-21

### Added

* Index mappings for Sumologic
* Malicious cmdlets in mdatp
* QRadar support for keyword searches
* QRadar mapping improvements
* QRadar field selection
* QRadar type regex modifier support
* Elasticsearch keyword field blacklisting with wildcards
* Added dateField configuration parameter in xpack-watcher backend
* Field mappings in configurations
* Field name mapping for conditional fields
* Value modifiers:
    * utf16
    * utf16le
    * wide
    * utf16be

### Changed

* Improved --backend-config help text

### Fixed

* Backend errors in ala
* Slash escaping within es-dsl wildcard queries
* QRadar backend config
* QRadar field name and value escaping and handling
* Elasticsearch wildcard detection pattern
* Aggregation on keyword field in es-dsl backend

## 0.12.1 - 2019-08-05

### Fixed

* Missing build dependency

## 0.12 - 2019-08-01

### Added

* Usage of "Channel" field in ELK Windows configuration
* Fields to mappings
* xpack-watcher actions index and webhook
* Config for Winlogbeat 7.x
* Value modifiers
* Regular expression support

### Changed

* Warning/error messages
* Sumologic value cleaning
* Explicit OR for Elasticsearch query strings
* Listing of available configurations on missing configuration error

### Fixed

* Conditions in es-dsl backend
* Sumologic handling of null values
* Ignore timeframe detection keyword in all/any of conditions
