# Front-end Style Guide

This is our front-end style guide to help devoloper in his tasks.

## VS-Code Prettier:

Use prettier[ extension-id : esbenp.prettier-vscode ] for code formatting.

For download prettier On VS-Code follow the below process:

1. Go to Extensions with shortcut keys CTRL + SHIFT + X.

2. Search for “Prettier” as shown below the image.

![prettier-extension](https://github.com/MTechZilla/style-guide/blob/dev/images/prettier-extension.png)

After successfully installing prettier on your VS-Code configure Prettier as per the following rules:

    *Tab has 4 spaces.
    *quotes should be double

“For configuring prettier go to settings icon then hit setting option search for prettier then select on prettier in Extensions section following UI will be open then configure it. ( configure process solution may vary with vs code versions if this process not worked search it on google).”
![prettier-config](https://github.com/MTechZilla/style-guide/blob/dev/images/prettier-config.png)

## VS-Code Configurations and extensions:

-   Eslint

-   Prettier [publisher:"Prettier"]

-   ES7 React/Redux/GraphQL/React-Native snippets [publisher:"dsznajder"]

-   GitLens — Git supercharged [publisher:"GitKraken"]

-   JavaScript (ES6) code snippets [publisher:"charalampos karypidis"]

-   Short keys documentation
    -   Format document CTRL + SHIFT + I
    -   Organize imports CTRL + SHIFT + O

## Web Vitals:

What is Web Vitals? ["Web Vitals is an initiative by Google to provide unified guidance for quality signals that are essential to delivering a great user experience on the web." ](https://www.google.com)

Rules for web vitals:

    * First time load: 2s
    * Largest content full paint: 1s
    * First Input Delay: NA
    * Cumulative layout shift: NA

For checking web scores use lighthouse on the google chrome browser

## Responsive Breakpoints:

-   480px

-   640px

-   768px

-   1024px

-   1280px

-   1536px

## Media:

For Media type of image only:
Single image file must be less than 50-60px.

    Following has image compression info you can use it for compress image

    JPG vs JPEG
          There is no difference between the .jpg and .jpeg filename extensions. Regardless of how you name your file, it is still the same format and will behave           the same way.
          The only reason that the two extensions exist for the same format is because .jpeg was shortened to .jpg to accommodate the three-character limit in               early versions of Windows. While there is no such requirement today, .jpg remains the standard and default on many image software programs.

          PNG - Portable Network Graphics

          PNGs are amazing for interactive documents such as web pages but are not suitable for print. While PNGs are "lossless," meaning you can edit them and             not lose quality, they are still low resolution.

          This is diff between jpeg and png

          The reason PNGs are used in most web projects is that you can save your image with more colors on a transparent background. This makes for a much                 sharper, web-quality image.

Resources for media:

-   https://undraw.co/
-   https://react-icons.github.io/react-icons/

## Coding standards:

1. Reusable components: Create a Component and use it as a template in the whole project. prefer --> [Condinglead](https://codinglead.co/javascript/what-is-DRY-code)
2. Casing:

    - UpperCamelCase: class / interface / type / enum / decorator / type parameters

    - lowerCamelCase: variable / parameter / function / method / property / module alias

    - CONSTANT_CASE global constant values, including enum values

## Code Commit:

The Conventional Commits specification is a lightweight convention on top of commit messages. It provides an easy set of rules for creating an explicit commit history; which makes it easier to write automated tools on top of.

The commit message should be structured as follows:

**Conventional commits**:

```bash
<type>[optional scope]: <description>
[optional body]
[optional footer(s)]
```

The commit contains the following structural elements, to communicate intent to the consumers of your library:

-   fix: a commit of the type fix patches a bug in your codebase (this correlates with PATCH in Semantic Versioning).
-   feat: a commit of the type feat introduces a new feature to the codebase (this correlates with MINOR in Semantic Versioning).
-   BREAKING CHANGE: a commit that has a footer BREAKING CHANGE:, or appends a ! after the type/scope, introduces a breaking API change (correlating with MAJOR in Semantic Versioning). A BREAKING CHANGE can be part of commits of any type.
-   types other than fix: and feat: are allowed, for example, @commitlint/config-conventional (based on the Angular convention) recommends build:, chore:, ci:, docs:, style:, refactor:, perf:, test:, and others.
-   footers other than BREAKING CHANGE: <description> may be provided and follow a convention similar to git trailer format.

You can refer:

1. [Coventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)
2. [How to write git commit message](https://chris.beams.io/posts/git-commit/)
