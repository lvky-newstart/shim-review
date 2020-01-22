Make sure you have provided the following information:

 - [*] link to your code branch cloned from rhboot/shim-review in the form user/repo@tag
	https://github.com/lvky-newstart/shim-review
 - [*] completed README.md file with the necessary information
	https://github.com/lvky-newstart/shim-review/blob/master/README.md
 - [*] shim.efi to be signed
	https://github.com/lvky-newstart/shim-review/blob/master/shimx64.efi
 - [*] public portion of your certificate embedded in shim (the file passed to VENDOR_CERT_FILE)
	https://github.com/lvky-newstart/shim-review/blob/master/NSDL_codesign.crt
 - [*] any extra patches to shim via your own git tree or as files
	none
 - [*] any extra patches to grub via your own git tree or as files
	none
 - [*] build logs
	https://github.com/lvky-newstart/shim-review/blob/master/build.log

###### What organization or people are asking to have this signed:
`[Guangdong Zhongxing Newstart Technology Co. ,Ltd]`

###### What product or service is this for:
`[Newstart Desktop Linux V3.3.6rc1]`

###### What is the origin and full version number of your shim?
`[15-1]`

###### What's the justification that this really does need to be signed for the whole world to be able to boot it:
`[We're OS vendor]`

###### How do you manage and protect the keys used in your SHIM?
`[Shim has the public key of the EV Code Signing key pair built-in and the key is used to validate GRUB boot loader. No private keys are embedded.Shim binary itself is signed, so the built-in public key cannot be modified or removed without making the signature invalid]`

###### Do you use EV certificates as embedded certificates in the SHIM?
`[Yes]`

###### What is the origin and full version number of your bootloader (GRUB or other)?
`[Source code origin is come from  http://www.gnu.org/software/grub/ and full version number is 2.02-0.38]`

###### If your SHIM launches any other components, please provide further details on what is launched
`[Yes, the boot loader(GRUB)]`

###### How do the launched components prevent execution of unauthenticated code?
`[They don't launch other code.]`

###### Does your SHIM load any loaders that support loading unsigned kernels (e.g. GRUB)?
`[No]`

###### What kernel are you using? Which patches does it includes to enforce Secure Boot?
`[The Fedora Linux kernel includes secure boot patches]`

###### What changes were made since your SHIM was last signed?
`[None]`

###### What is the hash of your final SHIM binary?
`[14926a652a6694fdaac1096261b4c07a961776f7c9997b5a668d7b27d6c3c5aa]`
