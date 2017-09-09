# dev-quick-refs
Quick life saving developer commands, hacks and lessons

#### Convert a .cer to .pem file

```bash
openssl x509 -inform der -in certificate.cer -out certificate.pem
```

#### Compress an entire directory or file
```bash
tar -czvf name-of-archive.tar.gz /path/to/directory-or-file
```
```txt
-c: Create an archive.
-z: Compress the archive with gzip.
-v: Verbose mdoe. Show progress
-f: Allows you to specify the filename of the archive.
```

#### Extract an archive
```bash
tar -xzvf archive.tar.gz -C /tmp
```
```txt
-C: Location to Extract archive to
```

#### Is the server running on host "localhost" and accepting TCP/IP connections on port 5432? (Mac)
First Try run this
```bash
rm /usr/local/var/postgres/postmaster.pid && pg_ctl -D /usr/local/var/postgres -l /usr/local/var/postgres/server.log start
```

if the above fails, then brew rescue your pg!
```bash
brew tap gapple/services
brew services start postgresql
```
