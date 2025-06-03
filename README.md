# oss-license-reporter

generate list of oss used in a project, including license text and notices

## Idea

OSS is awesome, but keeping your project compliant with license requirements is often not as easy as adding it to your code base.

There are ways to list dependencies, list licenses and also projects to generate license reports to inlcude in your project (shoutout to great projects like https://github.com/CycloneDX, https://github.com/aquasecurity/trivy, https://github.com/DependencyTrack/dependency-track and many more), but your stack might not match, commercial solutions might be to expensive, etc.

With this project I want to document my learnings and provide an extensible tool for generating license reports to keep your project complient with the license of used dependencies.

Expected features:
* for various languages (starting with those required for my day job)
  * scan dependencies for base license (e.g. MIT Licenes, Apache 2.0 License, etc.), provide license text, provide additional content like notice text to comply with Apache 2.0
  * scan source, if dependency doesn't directly provide license information (e.g. for elixir a dependency in deps doesn't contain the license file) and link to vcs is detected (e.g. link to github) 
  * warn
    * if license can't be detected
    * if detected copyleft licenses
  * generate listing (probably Erlang term format, JSON, html table and markdown table)
* provide guide for adding support for more languages
* provide github action, to include in CI/CD

## Disclaimer

* this is a hobby project in my free time and is not associated with any company
* it is licensed under the permissive MIT open-source license, but without warranty of any kind, see LICENSE file
