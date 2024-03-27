# Imcrypt: Encrypt and Decrypt Your Images Securely

Imcrypt is a powerful command-line interface (CLI) tool designed to encrypt and decrypt PNG, JPG, and JPEG images, providing you with complete control over your sensitive image files. With Imcrypt, you can protect your images with encryption and easily unlock them later using the generated key.


## Tech Stack

- ![Node](https://img.shields.io/badge/NodeJS-05122A?style=for-the-badge&logo=node.js)

## Preview

![Imcrypt Preview](https://github.com/Raghibhabib007/-Imcrypt/assets/163768743/4b0aaf57-8d0c-4dd4-bea0-957d953ecdb1)

## Installation

```sh
npm i -g imcrypt
```

## Usage

```sh
imcrypt <command> [option]
```

or run it directly using npx

```sh
npx imcrypt <command> [option]
```

### Commands

```sh
help  #prints help info
```

### Options

```sh
  -e, --encrypt              # Encrypt an image
  -d, --decrypt              # Decrypt an image
  -c, --clear                # Clear the console Default: false
  --noClear                  # Don't clear the console Default: true
  -v, --version              # Print CLI version Default: false
  -k, --key                  # Specify the decryption key Default: false
  -i, --outputImageFileName  # Specify the output image file name
  -p, --outputKeyFileName    # Specify the output key file name
```

## Examples

### Encrypting an Image

```sh
imcrypt -e myImage.png -i encryptedImageName.png -p keyFile.txt
```

### Decrypting an Image

```sh
imcrypt -d encryptedImage.png -k key.txt -i decryptedImage.png
```

## Output Example

```sh
Imcrypt v0.0.1 by theninza
An image encryption node-js cli

✔ Image read successfully
✔ Output image file name is valid
✔ Output key file name is valid
✔ Image data read successfully
✔ Key generated successfully
✔ Image encrypted successfully
✔ Image saved successfully
✔ Key saved successfully

✔  Image encrypted successfully:
                                  Encrypted image: encryptedImageName.png
                                  Key: keyFile.txt


```

## Limitations

While encryption and decryption work perfectly on PNG images, there are some limitations with JPG and JPEG images. These formats are lossy, and during encryption and decryption, a few pixel values may change. The decrypted image is very similar to the original, but with minor pixel changes.
