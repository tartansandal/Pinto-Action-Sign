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

# AUTHOR

Kahlil (Kal) Hodgson <kahlil.hodgson@dealmax.com.au>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2015 by Kahlil (Kal) Hodgson.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.

# POD ERRORS

Hey! **The above document had some coding errors, which are explained below:**

- Around line 53:

    You forgot a '=back' before '=head1'
