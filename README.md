<p align="center"><a href="http://www.dendoink.com" style="display: flex;
    justify-content: center;" target="_blank" rel="noopener noreferrer"><img style="width: 20%;
    height: 100%;border-radius: 3%;" src="http://ww1.sinaimg.cn/large/88b26e1cly1fz2gxpm5c0j215o0dwjrb.jpg" alt="Align logo"></a></p>

> A beautiful blog generator

### Project instruction

[-> Project description @digjin](https://juejin.im/post/5b53f9c4e51d4513ee6dcd3f)<br>

### Push configuration

1. dist Push: in the directory `@/config/index.js` Configure the following fields:

```javascript
module.exports = {
  //The compiled directory corresponds to the remote repository.
  //By default, you have an SSH key configured for the remote repository.
  distOriginSSh: 'git@github.com:xxx/xxx-blog-xxx.git'
};
```

> After configuration, `npm run build` will put `dist` push the code below to the address `git@github.com:xxx/xxx-blog-xxx.git` Corresponding warehouse

2. `commit` record information: default is` npm run build` If you append other information after `build`, this part of information will be submitted as a commit message.
    > If you want to customize the content of the commit message, you can configure the `commitMessage` property in `@/config/index.js`

```javascript
module.exports = {
  // commit messgae
  commitMessage:
    process.argv.length === 3
      ? `${process.argv[2]}:[${moment().format(
          'dddd, MMMM Do YYYY, h:mm:ss a'
        )}]`
      : `AutoUpdate:[${moment().format('dddd, MMMM Do YYYY, h:mm:ss a')}]`
};
```

3. Displayed name

- Configure the following information in `@/config/index.js`

```javascript
comments: {
    // commetsRepo : 'gihubusername/comments存储的仓库名'
    repo: '',
    // github-light | github-dark theme
    theme: 'github-light'
  },
```

- Configure [utteranc](https://utteranc.es/) related information

4. Personal information configuration

```javascript
userInfo: {
    name: 'name',
    phone: '1XX-XXXX-XXXX',
    site: 'www.yoursite.com',
    email: 'youemail@xmail.com',
    birth: 'December 10,1991',
    skills: [
      { label: 'HTML', percentage: '80%' },
      { label: 'CSS3', percentage: '60%' },
      { label: 'Javascript', percentage: '60%' },
      { label: 'jQuery', percentage: '50%' },
      { label: 'React', percentage: '60%' },
      { label: 'Vue', percentage: '60%' },
      { label: 'Mini-Program', percentage: '60%' },
      { label: 'Git', percentage: '70%' },
      { label: 'Webpack', percentage: '50%' }
    ],
    // Your city
    location: 'Shanghai,CN',
    // position
    jobTitle: 'Frontend Developer',
    // personal description
    description: 'Things we do are all for love'
  },
```

5. Landing Page configuration

```javascript
 ladingInfo: {
    // landing Displayed name
    blogName: 'Dendionk',
    tagA: 'Dreamer',
    tagB: 'Coder',
    tagC: 'Writter',
    github: '',
    twitter: '',
    email: '',
    linkedIn: ''
  },
```

6. Main warehouse push: no configuration field is provided, the current warehouse defaults to the main warehouse

7. Server configuration: Automatically pull the updated code [to be added]

### Preview local and upload test after configuration

```bash
# install dependencies
yarn

# debugging
yarn dev

# Package and push code to the corresponding warehouse
yarn build
```

### Blog Syntax Markdown Description

[->Syntax link](https://github.com/DendiSe7enGitHub/vue-blog-generater/blob/master/markdown.md)

### Features in development

<table>
  <tr>
    <th>Features</th>
    <th>Progress</th>
    <th>Last updated time</th>
  </tr>
  <tr>
    <td>Resume page</td>
    <td>Development completed </td>
    <td>2018-11-30</td>
  </tr>
  <tr>
    <td>Comment system</td>
    <td>Connected to [utteranc](https://utteranc.es/)</td>
    <td>2018-12-06</td>
  </tr>
  <tr>
    <td>Friendly chain</td>
    <td>Style and form to be determined</td>
    <td>2018-12-06</td>
  </tr>
  <tr>
    <td>Reward page</td>
    <td>Style and form to be determined</td>
    <td>2018-12-06</td>
  </tr>
  <tr>
    <td>Automated deployment</td>
    <td>Complete: After npm run build, it will be automatically pushed to the corresponding warehouse. Combined with the corresponding hosting platform hooks, local compilation has been implemented-> remote server update</td>
    <td>2018-12-06</td>
  </tr>
   <tr>
    <td>photo gallery</td>
    <td>Done</td>
    <td>2019-01-15</td>
  </tr>
  <tr>
    <td>Cancel the previous article and change to a recommended reading</td>
    <td>Form style designing</td>
    <td>2019-01-15</td>
  </tr>
</table>

There are more good suggestions, welcome pr or issue, there are still many shortcomings in this blog generation system, and it will be maintained. <br>

Everyone can find me on my [nugget account](https://juejin.im/user/585a2f52128fe10069ba1b95), and you are also welcome to communicate with me by email `dendise7en@gmail.com`


### Welcome to pay attention to the public number "front-end bully", scan the code to pay attention, good goods are waiting for you ~

![](https://user-gold-cdn.xitu.io/2019/3/20/169992ac3759e2d2?w=258&h=258&f=jpeg&s=27199)
