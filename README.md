# Fuse Archetype

This is a simple archetype that generates the skeleton for a JBoss Fuse project.

## OSGi Development

In order to export packages from bundles, you just need to define the property `osgi.export.packages`
and the profile for defining them in the Manifest will be activated.

## Feature Project

There is a separated project with an empty `features.xml` for defining your features. The reason is
to not make your bundles aware of the existence of others. By having a specific feature module you
can centralize all the awareness into one single project.

## JBoss Fuse Repositories

The parent already provides the JBoss Fuse repositories (needed as of JBoss Fuse 6.3). The recomendation
is to not depend on specific repositories for your project. They should be available to you either
by having a mirror like Nexus or Artifactory or by having the repositories mapped in your Maven
Settings File. Since the goal of this archetype is to provide a "batteries included" structure, the
repositories are defined in the parent pom.

## Plugin Versions

If you don't provide versions for some plugins like `maven-compiler-plugin`, Maven will fetch the
latest available. This parent pom defines versions for almost every `maven-*-plugin` you need to
start developing your bundles.

## Test Dependencies

Since our codes should be testes, the parent already contains dependencies for nice test frameworks.
