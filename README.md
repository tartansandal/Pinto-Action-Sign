# NAME

App::Pinto::Command::sign - sign all the checksums files in the repository

# VERSION

version 0.001

# SYNOPSIS

    pinto --root=REPOSITORY_ROOT sign [OPTIONS] key

# DESCRIPTION

This command signs the checksums files for all distributions defined in the
repository. This is similar to what PAUSE does.  Currently we only support
GnuPG.

# COMMAND ARGUMENTS

This command requires a single key identifier to specify the key to be used
with signing.  This could be the 8 character keyid of the full, quoted key
fingerprint.

# COMMAND OPTIONS

- --gpg-homedir=PATH
- -d PATH

    Specifies the path to the GnuPG homedir containing the desied keyring and trustdb.

- --program-string=STRING
- -p STRING

    Specify the program string used to clearsign a file.  This defaults to:

        "gpg2 --clearsign --default-key"

    Note, that the key identifier will be appended to this invokation.

    You will want to ensure that this command hooks into your gpg user agent
    appropriately, otherwise, you will have to enter your keys passphrase many
    times.

# SUPPORT

## Perldoc

You can find documentation for this module with the perldoc command.

    perldoc App::Pinto::Command::sign

## Websites

The following websites have more information about this module, and may be of help to you. As always,
in addition to those websites please use your favorite search engine to discover more resources.

- MetaCPAN

    A modern, open-source CPAN search engine, useful to view POD in HTML format.

    [http://metacpan.org/release/Pinto-Action-Sign](http://metacpan.org/release/Pinto-Action-Sign)

- Search CPAN

    The default CPAN search engine, useful to view POD in HTML format.

    [http://search.cpan.org/dist/Pinto-Action-Sign](http://search.cpan.org/dist/Pinto-Action-Sign)

- RT: CPAN's Bug Tracker

    The RT ( Request Tracker ) website is the default bug/issue tracking system for CPAN.

    [https://rt.cpan.org/Public/Dist/Display.html?Name=Pinto-Action-Sign](https://rt.cpan.org/Public/Dist/Display.html?Name=Pinto-Action-Sign)

- AnnoCPAN

    The AnnoCPAN is a website that allows community annotations of Perl module documentation.

    [http://annocpan.org/dist/Pinto-Action-Sign](http://annocpan.org/dist/Pinto-Action-Sign)

- CPAN Ratings

    The CPAN Ratings is a website that allows community ratings and reviews of Perl modules.

    [http://cpanratings.perl.org/d/Pinto-Action-Sign](http://cpanratings.perl.org/d/Pinto-Action-Sign)

- CPAN Forum

    The CPAN Forum is a web forum for discussing Perl modules.

    [http://cpanforum.com/dist/Pinto-Action-Sign](http://cpanforum.com/dist/Pinto-Action-Sign)

- CPANTS

    The CPANTS is a website that analyzes the Kwalitee ( code metrics ) of a distribution.

    [http://cpants.cpanauthors.org/dist/Pinto-Action-Sign](http://cpants.cpanauthors.org/dist/Pinto-Action-Sign)

- CPAN Testers

    The CPAN Testers is a network of smokers who run automated tests on uploaded CPAN distributions.

    [http://www.cpantesters.org/distro/P/Pinto-Action-Sign](http://www.cpantesters.org/distro/P/Pinto-Action-Sign)

- CPAN Testers Matrix

    The CPAN Testers Matrix is a website that provides a visual overview of the test results for a distribution on various Perls/platforms.

    [http://matrix.cpantesters.org/?dist=Pinto-Action-Sign](http://matrix.cpantesters.org/?dist=Pinto-Action-Sign)

- CPAN Testers Dependencies

    The CPAN Testers Dependencies is a website that shows a chart of the test results of all dependencies for a distribution.

    [http://deps.cpantesters.org/?module=App::Pinto::Command::sign](http://deps.cpantesters.org/?module=App::Pinto::Command::sign)

## Bugs / Feature Requests

[https://github.com/tartansandal/Pinto/issues](https://github.com/tartansandal/Pinto/issues)

## Source Code

The code is open to the world, and available for you to hack on. Please feel free to browse it and play
with it, or whatever. If you want to contribute patches, please send me a diff or prod me to pull
from your repository :)

[https://github.com/tartansandal/Pinto](https://github.com/tartansandal/Pinto)

    git clone git://github.com/tartansandal/Pinto.git

# AUTHOR

Kahlil (Kal) Hodgson <kahlil.hodgson@dealmax.com.au>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2015 by Kahlil (Kal) Hodgson.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.
