# Writting good documentation

## Step 1 - Using codeblocks.

Codeblocks in markdown make it *very easy* for tech people to copy, paste, share code.
**A good Cloud Engineer uses Codeblocks whenever possible**, because it allows others to copy and paste their code to replicate or research issues.

If you need to show a codeblock, use 3 backticks (```):

```
provider "aws" {
  region = "us-east-1"
  profile = "sandbox"
}

resource "aws_instance" "example" {
  ami           = "ami-08c40ec9ead489470"
  instance_type = "t2.micro"

  tags = {
    Name = "terraform-2023-example"
  }
}
```
Now, a good idea is to indicate what programming language you are using, so that it shows colored highlighting:

```terraform
provider "aws" {
  region = "us-east-1"
  profile = "sandbox"
}

resource "aws_instance" "example" {
  ami           = "ami-08c40ec9ead489470"
  instance_type = "t2.micro"

  tags = {
    Name = "terraform-2023-example"
  }
}
```
Good Cloud Engineers also use codeblocks to show errors that appear in their console:

```bash
$ ls /nonexistent_directory
ls: cannot access '/nonexistent_directory': No such file or directory
```
> This is an example error output on a Linux console.

## Step 2 - Use GitHub Flavoured Markdown Task Lists

GitHub extendes Markdown to have a list where you can check off items.
- [X] Finish Step 1.
- [X] Finish Step 2.
- [x] Finish Step 3.

## Step 3 - Use Emojis (and tables)

GitHub Flavoured Markdown (GFM) supports emoji shortcodes. Here are some examples:

| Name | Shortcode | Emoji |
| --- | --- | --- |
| Cloud | `:cloud:` | :cloud: |
| Abacus | `:abacus:` | :abacus: |


## Citing references

You can show the URLs:
- https://openai.com/blog/chatgpt
- https://workshops.aws/

Or you can show more friendly names:
- [Example code snippets](https://openai.com/blog/chatgpt)
- [Reference architectures on AWS](https://workshops.aws/)
