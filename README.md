# Kerberos Utilities

The following will read the Kerberos configuration in `/etc/krb5.conf`.
This can be overridden with the environment variable `KRB_CONF`.

## `make-keytab`

Usage:

    make-keytab [USERNAME]

Create a Kerberos keytab for `USERNAME` (defaults to the current user)
in the default Kerberos realm. This will ask you for your password and
create a keytab named `USERNAME.keytab` in the working directory, using
the realm's supported ciphers.

## `renew-keytab`

Usage:

    renew-keytab [USERNAME] [KEYTAB]

Renew the Kerberos keytab file given by `KEYTAB` (defaults to
`USERNAME.keytab`) for 7 days, for `USERNAME` (defaults to the current
user).

## `init-keytab`

Usage

    init-keytab [USERNAME] [KEYTAB]

Initialise ("log in") the Kerberos session using the keytab file given
by `KEYTAB` (defaults to `USERNAME.keytab`), for `USERNAME` (defaults to
the current user).
