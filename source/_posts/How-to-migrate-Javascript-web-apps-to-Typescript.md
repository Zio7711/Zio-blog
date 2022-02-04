---
title: How to migrate JavaScript web apps to Typescript
date: 2022-02-04 19:45:48
tags: [Typescript, JavaScript]
---

Quite fascinated with the “Typescript” at first, I quickly realized that it is just my old pal JavaScript with advanced implementation. In technical terms, TypeScript is a programming language based on JavaScript. JS lacked some necessary features such as object orientation, type-checking, and compile-time error checks needed to develop more extensive applications.

The code written in TypeScript is eventually converted into Javascript using a transpiler. Therefore, Typescript has all the features of JavaScript with added features of a type system.

Unlike JS, TS helps us structure our programs, define fixed data types, provide access to interfaces, classes, generics, modules, and enumerated types. In short, TS helps us increase our productivity as developers by reducing the time taken to locate and correct errors. This article will help you in migrating Javascript-based web apps to Typescript web apps.

Even though it’s a bit long process, it’s completely worth your time, and converting your existing project will be the best way to learn Typescript.

# How to Migrate JS-based apps to TypeScript

The best way to tackle any daunting task is to break it down into simpler parts. Also known as Divide and Conquer method😜😜, which I always find helpful while tackling a big task. Here is a step-by-step breakdown –

# 1. Add Typescript

As Typescript can run with the existing javascript code compilers of our project, we just need to add Typescript as

![img](https://miro.medium.com/max/30/1*Sws9A5LZ4F2CWZEmTOhrRQ.png?q=20)

![img](https://miro.medium.com/max/700/1*Sws9A5LZ4F2CWZEmTOhrRQ.png)

Or if you use Yarn –

![img](https://miro.medium.com/max/30/1*-faRxGfJEwVZoNsaYkt_fQ.png?q=20)

![img](https://miro.medium.com/max/700/1*-faRxGfJEwVZoNsaYkt_fQ.png)

So what will this step do to our project? NOTHING, Nothing at all! The reason is that we are just adding another library to our project. But we haven’t used it or done anything on it yet. Let’s go to the implementation part.

# 2. Add the tsconfig.json

TypeScript manages projects using a [*tsconfig.json*](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html) file. It contains options like which files need to be included and which type of checking should be done. Basically, we declare the rules on which our type checking will work. You can simply add tsconfig.json file as –

![img](https://miro.medium.com/max/30/1*J3GsLWbIVUiOfKoOrUj0rQ.png?q=20)

![img](https://miro.medium.com/max/700/1*J3GsLWbIVUiOfKoOrUj0rQ.png)

After adding the [*tsconfig.json*](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html) file, either you can leave it as it is and move to the next steps or edit it and specify the following things to TypeScript:

1. ***Read in any files it understands in the src directory (with\*** [***include\***](https://www.typescriptlang.org/tsconfig#include)***).\***
2. ***Accept JavaScript files as inputs (with\*** [***allowJs\***](https://www.typescriptlang.org/tsconfig#allowJs)***).\***
3. ***Emit all the output files in the created folder (with\*** [***outDir\***](https://www.typescriptlang.org/tsconfig#outDir)***).\***
4. ***Translate newer JavaScript constructs down to an older version (using\*** [***target\***](https://www.typescriptlang.org/tsconfig#target)***).\***

# 3. Start with a Simple Component

The best part of typeScript is that it can exist with JS in the same folder, so you don’t need to convert everything at once, and you can easily convert one file at a time. To begin the migration, migrate the leaf level file first (files that don’t have other dependent files). Now, you need to perform the following steps –

1. ***Change the file extension to .ts or .tsx\***
2. ***Add the type annotation\***

As this file will be expecting some props from its parent files, you have to define the Props type, as

![img](https://miro.medium.com/max/30/1*SGntCpV6hCeOy8q20isADg.png?q=20)

![img](https://miro.medium.com/max/700/1*SGntCpV6hCeOy8q20isADg.png)

Now, double-check if this file is complied properly, by building the project.

In react case, react-scripts will automatically detect the new file configuration and update our ts-config accordingly.

While migrating bigger files, you may find some additional packages dependent on 3rd party libraries that we are using that give a type error for eg [Moment library](https://momentjs.com/). To remove this, just add the type for that library as a dev dependency. Like –

![img](https://miro.medium.com/max/30/1*D-2N7u4lEBmedFUIP2nGeQ.png?q=20)

![img](https://miro.medium.com/max/700/1*D-2N7u4lEBmedFUIP2nGeQ.png)

You can easily find the type dependencies by searching the error over google. Even if you cannot fix the error, you can add [***// @ts-ignore\***](https://www.typescriptlang.org/docs/handbook/release-notes/typescript-2-6.html#suppress-errors-in-ts-files-using--ts-ignore-comments) on the line before the error so that TS will ignore this error line and you can easily build your project.

In the case of React, do remember that react uses [JSX](https://reactjs.org/docs/introducing-jsx.html), so in place of declaring the file as .ts, you should declare it as .tsx. It will remove the majority of your errors while compiling the JSX file.

Repeat this process again and again with the remaining files, and you are good to go. Just remember that TS is designed to increase the developer’s productivity, so don’t stick on a single file for too long. Otherwise, you will be stuck forever.

# 4. Now What?

![img](https://miro.medium.com/max/30/0*WRvBQPNVOO29-33n?q=20)

![img](https://miro.medium.com/max/700/0*WRvBQPNVOO29-33n)

TS is like our neighborhood wizard friend, which helps us in a certain way to avoid errors. It doesn’t let errors pass into production code and keeps our code nice, tidy, and error-proof. To make it more strict with errors, you can always implement stricter rules in our tsconfig.json file. (You should visit the [Typescript documentation](https://www.typescriptlang.org/docs/handbook/intro.html) for a better understanding of TS rules) Implement them in the tsconfig.json file, build your project and fix those errors. You can enable the below rules one by one –

- ***“\***[***noImplicitAny\***](https://www.typescriptlang.org/tsconfig#noImplicitAny)***”: true\***
- ***“\***[***strictNullChecks\***](https://www.typescriptlang.org/tsconfig#strictNullChecks)***”: true\***
- ***“\***[***noImplicitThis\***](https://www.typescriptlang.org/tsconfig#noImplicitThis)***”: true\***
- ***“\***[***alwaysStrict\***](https://www.typescriptlang.org/tsconfig#alwaysStrict)***”: true\***

If you find some errors related to the type and can’t understand it, just provide a type of [***any\***](https://www.typescriptlang.org/docs/handbook/intro.html) to that, move on, and fix that error later. After all, migration is being done to increase productivity and not to waste time.

Once you are done with resolving the errors from the above rule, add a single rule as [***“strict”: true\***](https://www.typescriptlang.org/tsconfig)

And remove all the other, this will automatically enable all the error check mentioned above and also enables other checks such as –

- [***strictBindCallApply\***](https://www.typescriptlang.org/tsconfig#strictBindCallApply)
- [***strictNullChecks\***](https://www.typescriptlang.org/tsconfig#strictNullChecks)
- [***strictFunctionTypes\***](https://www.typescriptlang.org/tsconfig#strictFunctionTypes)
- [***strictPropertyInitialization\***](https://www.typescriptlang.org/tsconfig#strictPropertyInitialization)

This makes your tsconfig.json quite strict, and if you want to go further, just add the following –

- **“noUnusedLocals”: true**
- **“noUnusedParameters”: true**
- **“noImplicitReturns”: true**
- **“noFallthroughCasesInSwitch”: true**

Although I don’t suggest this level of strictness as this can act as a blocker to new developers working on the project. However, it’s your decision after all.

# You are now done with the migration. Take a break and enjoy 🎉

Migration is quite a big task, and you did it, so you must pat your back and enjoy it till you are assigned to a new project to migrate.😊😊

Remember to learn TS in this process. You can learn several advanced concepts like — Generics, Keyof Type operator, Typeof Type operator, conditional types, mapped types, template literal types, Utility types, etc. These concepts help us create reusable pieces of code and define several data types, which was otherwise not possible. Creating conditions, avoiding repetition in code, and establishing a relationship between input and output types. You can easily write complex programs and define numerous data types without any syntax restrictions.

# Conclusion:

[TypeScript](https://www.typescriptlang.org/) has helped become [JavaScript](https://www.javascript.com/) a complete language. You can import components from the TypeScript library and easily develop complex applications. The demand for this language is continuously growing owing to the simple syntax and easily readable and understandable programs. So enjoy this journey and give a thumbs up if you like this article.



