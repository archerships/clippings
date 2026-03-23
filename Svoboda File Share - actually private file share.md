# Svoboda File Share - actually private file share
[Svoboda File Share - actually private file share](https://file.svoboda.center/) 

 Usage

File size limit: 10 GB.

Files auto-delete in 14 days, unless set as permanent ("Show image", for sale, or 10+ downloads).

We ignore DMCA requests.

You are solely responsible for any files you upload, as we do not check file contents.

Using strong password guarantees that only you can access the uploaded file - even we cannot access it.

Privacy

Zero log policy. No tracking. No KYC. Minimal JS and it's not required (used for showing progress bar).

We recommend using Tor Browser or at least VPN to upload files.

Encryption

Files are encrypted using XSalsa20 + Poly1305 + Argon2id (for password hashing).

The password is not stored. It is only used to encrypt the file.

If you forget the password, consider the file lost.

Files uploaded without a password are still encrypted using a server key.

API

This API allows you to upload and download files programmatically.

#### Endpoints:

*   **POST /upload**: Upload one or more files.
*   **GET /file/<unique\_id>**: Retrieve file information by its unique ID.
*   **GET /files/<group\_id>**: Retrieve all files in a group.
*   **POST /download/<unique\_id>**: Download a file by its unique ID.

#### Example Usage:

##### 1\. Upload a File:

```
curl https://file.svoboda.center/upload \
-F "files=@/path/to/your_file.txt" \
-F "password=your_password" \
-F "delete_after_download=true"
```

##### 2\. Retrieve File Info:

```
curl https://file.svoboda.center/file/<unique_id>?json=true
```

##### 3\. Retrieve Files in a Group:

```
curl https://file.svoboda.center/files/<group_id>?json=true
```

##### 4\. Download a File:

```
curl https://file.svoboda.center/download/<unique_id>?password=your_password -o your_file.txt
```

Note: The `password` and `delete_after_download` fields are optional.