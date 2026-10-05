# freemkv Unraid templates

Docker templates for running [freemkv-library](https://freemkv.org/docs/library/)
(the freemkv web server: insert a disc, get an MKV) on Unraid.

## Install

1. Unraid web UI → **Docker** → scroll to **Template Repositories** and add:

   ```
   https://github.com/freemkv/unraid-templates
   ```

   then **Save**.
2. **Docker** → **Add Container** → pick **freemkv-library** from the template list.
3. Check the paths (Config, Output, Staging, Keys) and **Apply**.
4. Open `http://<unraid-ip>:8080`.

Or, without adding the repository, paste the template directly:
`https://raw.githubusercontent.com/freemkv/unraid-templates/main/freemkv-library.xml`.

The container must stay **Privileged**; without it no optical drives are
detected. Blu-ray and UHD need [decryption keys](https://freemkv.org/docs/decryption-keys/).
