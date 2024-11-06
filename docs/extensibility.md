# Package Extensibility

This package provides many ways for developers to customise the behaviour.

## Ruleset overriding and adding custom rules

You can override or add custom rules to the config as follows.

```xml
<?xml version="1.0"?>
<ruleset>
	<!-- Exclude rules from specific ruleset -->
    <rule ref="vendor/newsuk/nuk-wp-phpmd-config/ruleset.xml">
		<exclude name="local-rulesets/cleancode.xml" />
	</rule>
	<!-- Excluding selected paths from being validated by phpmd -->
	<exclude-pattern>*/includes/some-directory/*</exclude-pattern>
	<!-- Import other rules into rule set -->
    <rule ref="local-rulesets/some-other-rule.xml" />
</ruleset>

```
