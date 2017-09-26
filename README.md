# Default eclipse settings

This module is used together with the `eclipse-settings-maven` plugin to distribute eclipse settings across out projects (i.e. to enforce common code style and compiler warnings).

## Maven plugin

Please add the following snippet to your project's maven setting to enforce these settings:

```xml
<plugin>
    <groupId>org.apache.maven.plugins</groupId>
    <artifactId>maven-eclipse-plugin</artifactId>
    <version>2.10</version>
    <configuration>
     <additionalConfig>
      <file>
        <name>.settings/org.eclipse.jdt.core.prefs</name>
        <url>https://raw.githubusercontent.com/weblyzard/eclipse-settings/master/settings/org.eclipse.jdt.core.prefs</url>
      </file>
      <file>
        <name>.settings/org.eclipse.jdt.ui.prefs</name>
        <url>https://raw.githubusercontent.com/weblyzard/eclipse-settings/master/settings/org.eclipse.jdt.ui.prefs</url>
      </file>
      </additionalConfig>
    </configuration>
</plugin>
```
