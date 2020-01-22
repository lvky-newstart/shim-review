This repo is for review of requests for signing shim.  To create a request for review:

- clone this repo
- edit the template below
- add the shim.efi to be signed
- add build logs
- commit all of that
- tag it with a tag of the form "myorg-shim-arch-YYYYMMDD"
- push that to github
- file an issue at https://github.com/rhboot/shim-review/issues with a link to your branch

Note that we really only have experience with using grub2 on Linux, so asking
us to endorse anything else for signing is going to require some convincing on
your part.

Here's the template:

-------------------------------------------------------------------------------
What organization or people are asking to have this signed:
-------------------------------------------------------------------------------
[Guangdong Zhongxing Newstart Technology Co. ,Ltd]

-------------------------------------------------------------------------------
What product or service is this for:
-------------------------------------------------------------------------------
[Newstart Desktop Linux V3.3.6rc1]

-------------------------------------------------------------------------------
What's the justification that this really does need to be signed for the whole world to be able to boot it:
-------------------------------------------------------------------------------
[We're OS vendor]

-------------------------------------------------------------------------------
Who is the primary contact for security updates, etc.
-------------------------------------------------------------------------------
- Name:lvkaiyi
- Position:Engineer
- Email address:lv.kaiyi@gd-linux.com
- PGP key, signed by the other security contacts, and preferably also with signatures that are reasonably well known in the linux community:
	https://github.com/lvky-newstart/shim-review/blob/master/lvkaiyi.pub
-------------------------------------------------------------------------------
Who is the secondary contact for security updates, etc.
-------------------------------------------------------------------------------
- Name:maizhuodong
- Position:Engineer
- Email address:mai.zhuodong@gd-linux.com
- PGP key, signed by the other security contacts, and preferably also with signatures that are reasonably well known in the linux community:
	https://github.com/lvky-newstart/shim-review/blob/master/mai.pub
-------------------------------------------------------------------------------
What upstream shim tag is this starting from:
-------------------------------------------------------------------------------
[https://github.com/rhboot/shim/tree/15]

-------------------------------------------------------------------------------
URL for a repo that contains the exact code which was built to get this binary:
-------------------------------------------------------------------------------
[https://github.com/lvky-newstart/shim-review/blob/master/shim-unsigned-x64-15-1.fc25.src.tar.gz]

-------------------------------------------------------------------------------
What patches are being applied and why:
-------------------------------------------------------------------------------
[None]

-------------------------------------------------------------------------------
What OS and toolchain must we use to reproduce this build?  Include where to find it, etc.  We're going to try to reproduce your build as close as possible to verify that it's really a build of the source tree you tell us it is, so these need to be fairly thorough. At the very least include the specific versions of gcc, binutils, and gnu-efi which were used, and where to find those binaries.
-------------------------------------------------------------------------------
[It's done on something very close to the Fedora 25. you can get the os in http://mail.gd-linux.com/attachment/gdown/NSDL-V3.3.6rc1-ZTE-x86_64.iso?itemid=netdiskid%3Av001%3Afile%3ADzzzzzzNqZr%3B7pXFTDB3tqaTxnQeq5tvfwq6JfPqYn8dx228yqp07rNX%2FIm2QehcGJBgHwUs0f81Qbk1Ljr9hf6OeW82QFmz9IxHNHRd2hybrPLi2DRQ8bM5ORhI%2BtGG%2B%2FtCQCYZdc3d .Before you build the source code, you should install rpm-build and other tollchain like gnu-efi-3.0.8-6.fc30.x86_64 in https://github.com/lvky-newstart/shim-review/blob/master/gnu-efi-3.0.8-6.fc30.x86_64.rpm and gnu-efi-devel-3.0.8-6.fc30.x86_64 in https://github.com/lvky-newstart/shim-review/blob/master/gnu-efi-devel-3.0.8-6.fc30.x86_64.rpm. After install the toolchain, Unzip shim-unsigned-x64-15-1.fc25.src.tar.gz to rpmbuild/SOURCES, run the command 'rpmbuild -ba shim-unsigned-x64.spec',you can get the rpm package in rpmbuild/RPMS.]

-------------------------------------------------------------------------------
Which files in this repo are the logs for your build?   This should include logs for creating the buildroots, applying patches, doing the build, creating the archives, etc.
-------------------------------------------------------------------------------
[https://github.com/lvky-newstart/shim-review/blob/master/build.log]

-------------------------------------------------------------------------------
Add any additional information you think we may need to validate this shim
-------------------------------------------------------------------------------
[None]
