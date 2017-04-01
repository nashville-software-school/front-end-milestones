# The Static Web HTML + CSS

## Setup

Run the following command in your terminal:

```bash
mkdir -p ~/workspace/exercises/the-static-web/productcards && cd $_
```

This will create a project folder and cd you into it.
+ Once your repository is created on GitHub, copy the list of commands under **"..or create a new repository on the command line"** by clicking on the clipboard icon
+ Paste the commands into your terminal. This will create a README.md file, add it, commit it, connect your local repo to GitHub, and set you up to push up the changes. (If the last command, `git push origin master` isn't automatically executed, hit enter/return to run it).

All of your work should be on a branch, NOT on master. To do this, type:

```bash
git checkout -b exercise
touch index.html
mkdir css && touch css/style.css
mkdir images
```

You are now ready to work in the `exercise` branch.

When your work is complete, push up the branch (`git push origin exercise`) and submit the pull request on Github.

## Requirements

Your task is to build a grid of cards for a company's products. Here are the requirements for the basic structure of the cards.

1. Each card should be an `article`.
1. Each card should take up 30% of the width of the browser window.
1. Each product should contain a `header` element that, itself, contains an `h2` element where the product's title will be written.
1. Each product should have three sections.
1. The first section should contain three child block elements.
    1. The first element contains the product image.
    1. The second element contains the product description.
    1. The third element contains the product availability (e.g. "Available" or "Not Available")
1. The second section contains product specifications.
    1. This section should have a header containing the word "Specifications"
    1. This section should contain two block elements
    1. The first block element specifies the size.
    1. The second block element specifies the weight.
    1. This section should contain a footer.
    1. The footer contains text stating when the product specifications become invalid.
1. The third section contains the product pricing.
    1. This section should contain a header.
    1. This section should contain three block elements.
    1. Each block element contains information about the price for different quantities.

### Additional style requirements

1. The entire card has a solid 1px border that is `lightblue`.
1. The card title has a dotted 1px border that is `lightgray`.
1. The title and product image are centered.
1. Notice that the text for the description in the image is justified.
1. The text for the product specification details and pricing details is bold.
1. The availability element extends the full width of the card, with a dark grey background and yellow text.

### Visual example

Here's an image that shows how the cards should appear.

![Static Web Product Cards Example](./SW_HTML_CSS_exercise.png)
