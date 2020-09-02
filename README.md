# Announcerr Github Action

Automatically announce and send mails to list of subscribers on every product release 🚀 

## Usage

```yaml
- name: Announcerr
  uses: singhkshitij/announcerr@v2
  with:
    server_address: smtp.gmail.com
    server_port: 465
    username: ${{secrets.MAIL_USERNAME}}
    password: ${{secrets.MAIL_PASSWORD}}
    subject: Launching my awesomeProduct version ${{ github.event.release.tag_name }}
    # Literal body:
    body: Just launched new version of my ${{github.repository}} ! It is fully packed with awesome features.
    # Read file contents as body:
    body: file://README.md
    to: user1@xyz.com,user2@abc.com
    from: Kshitij Singh # <kshitij@mytrashcode.com>
    # Optional content type (defaults to text/plain):
    content_type: text/html
    # Optional attachments:
    attachments: attachments.zip,git.diff,./dist/static/main.js
```
