# Ansible Amazon S3 Downloader

Role for ansible to download files from amazon

## Installation

Put this role in your "roles" folder

## Usage

This role has to be configured by the next variables:

Define the aws s3 region:

aws_s3_region: "us-east-1"

Define the user access key and secret key to access to your s3:

aws_s3_access_key: ""
aws_s3_secret_key: ""

Define the name of your bucket:

aws_s3_bucket: ""

Define the files to be downloaded with this structure:

aws_s3_get_files:
  - { object: ROUTE_S3_FILE , dest: DEST_LOCAL_SERVER }
  - ...

For example:

aws_s3_get_files:
  - { object: /daily/package.gz , dest: /tmp/test.gz }
  - { object: /daily/package2.tgz , dest: /tmp/test.tgz }

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## License

GNU GPLv3