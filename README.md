# Next.JS

## Goal: Complete the tutorial found [HERE](https://nextjs.org/learn/basics/navigate-between-pages/client-side) by adding each detailed step to this README.md as seen below AS WELL AS actually implementing each step you add to the README.md.

## This repository is for anyone trying to practice and learn NextJS while collaborating with others and earning those contributions that hiring teams look for!!! To make a contribution, please follow these steps:

## Making a contribution (PLEASE ADD TO THIS IF YOU HAVE BETTER INSTRUCTIONS!)
1. Fork the repo
2. Make changes (consider starting with small changes) that get our team closer to the goal: Completing the tutorial and deploying a NextJS React App! 
3. Create Pull Request and wait for an admin to verify the changes and merge the request. 

# NextJS React App Tutorial:

## Getting Started
Run the following commands in your terminal
```
npx create-next-app nextjs-blog --use-npm --example "https://github.com/vercel/next-learn/tree/master/basics/navigate-between-pages-starter"
```

```
cd nextjs-blog
```

```
npm run dev
```


## Pages
In Next.js, a page is a React Component exported from a file in the pages directory.

Pages are associated with a route based on their file name. For example, in development:

`pages/index.js` is associated with the `/` route.
`pages/posts/first-post.js` is associated with the `/posts/first-post route`.
We already have the pages/index.js file, so let’s create pages/posts/first-post.js to see how it works.

### Creating a new page
Create the `/posts` directory under `/pages`.

Create a file called `first-post.js` inside the `/posts` directory with the following content:
```
export default function FirstPost() {
  return <h1>First Post</h1>
}
```
The component can have ***any name***, but you must export it as a ***default export***.

This is how you can create different pages in Next.js.

## ✴️✴️✴️Simply create a JS file under the pages directory, and the path to the file becomes the URL path.✴️✴️✴️

In a way, this is similar to building websites using HTML or PHP files. Instead of writing `HTML` you write `JSX` and use `React Components`.

Let's add a `**link**` to the newly added page so that we can navigate to it from the homepage.

## Link Component
When linking between pages on websites, you use the `<a>` HTML tag.

In Next.js, you use the `Link Component` from next/link to wrap the `<a>` tag. `<Link>` allows you to do client-side navigation to a different page in the application.

### Using `<Link>`
1. Open pages/index.js
2. Import the Link component from next/link:
```
import Link from 'next/link'

```
3. Then find the h1 tag that looks like this:
```
<h1 className="title">
  Learn <a href="https://nextjs.org">Next.js!</a>
</h1>
```
4. And change it to:
```
<h1 className="title">
  Read{' '}
  <Link href="/posts/first-post">
    <a>this page!</a>
  </Link>
</h1>
```
##### Note: `{' '}` adds an empty space, which is used to divide text over multiple lines.
5. Next, open pages/posts/first-post.js and replace its content with the following:
```
import Link from 'next/link'

export default function FirstPost() {
  return (
    <>
      <h1>First Post</h1>
      <h2>
        <Link href="/">
          <a>Back to home</a>
        </Link>
      </h2>
    </>
  )
}

```

As you can see, the `Link` component is similar to using `<a>` tags, but instead of `<a href="…">`, you use `<Link href="…">` and put an `<a> `tag inside.

You should now have a link on each page, allowing you to go back and forth. Verify this before moving forward!




 


