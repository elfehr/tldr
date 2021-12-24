# mu

> Index and search emails from a local Maildir.
> More information: <https://www.djcbsoftware.nl/code/mu/>.

- Initialize the email database, optionally specifying the Maildir directory and email addresses belonging to self :

`mu init --maildir={{/path/to/directory}} --my-address={{name@example.com}}`

- Index new emails:

`mu index`

- Find messages with a keyword (in message body, subject, sender, ...)
`mu find {{keyword}}`

- Find messages to Alice with subject `jellyfish` containing the words `apples` or `oranges`:

`mu find to:{{alice}} subject:{{jellyfish}} {{apples}} OR {{oranges}}`

- Find unread messages about words starting with `soc` (the `*` only works at the end of the search term) in the Sent Items folder:
`mu find 'subject:{{soc}}*' flag:{{unread}} maildir:'{{/Sent Items}}'`

- Find messages from Sam with attached images, between 2kB and 2Mb, written in 2021:

`mu find 'mime:{{image/*}} size:{{2k..2m}} date:{{20210101..20211231}} from:{{sam}}`

- List contacts with `Bob` in either name or email address:

`mu cfind {{Bob}}`
