# Import

There are different way to import existing WordPress website.

## Import from duplicator archive

Install [duplicator plugin](https://wordpress.org/plugins/duplicator/) on your existing website. Go to admin part of your WordPress website and create a new package via duplicator.

Now navigate to `Apps > Deploy` and choose duplicator archive as data source on the 3rd step.

## Import from separate archives

Import WordPress via separate archives for database and files. We support `.zip`, `.gz`, `.tar.gz`, `.tgz` and `.tar` archives. This option is available on the 3rd step of a new instance deployment form and also on `[Instance] > Import` page of existing instance.

## Manual import

In case your import data is huge it makes sense to import it manually from the server. Follow these steps:

1. Deploy your WordPress website from a git repository without importing data
2. Once the app is deployed, go to `Stack > SSH` and copy SSH command
3. Connect to the container by SSH
4. Copy your database archive here via `wget` or `scp`, make sure it's gzipped
5. Import unpacked database dump using `wp db import my-db-dump.sql`
6. Now let's import your files, cd to `/mnt/files/public`
7. Copy your files archive here via `wget` or `scp` and unpack the archive
8. That's it! Clear WordPress cache and remove import artifacts

## Import between instances

You can import database and files from one instance to another regardless of whether instances are on the same server or not. Go to `[Instance] > Import` tab and select an instance where you'd like to import database/files from.
