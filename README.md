# Noobee CMS (Decap + GitHub Pages)

- Admin: `/admin`
- Backend: GitHub OAuth (implicit)
- Hosting: GitHub Pages
- Media: `/static/uploads` → `/noobee-cms/uploads`

## Setup
1. **Enable Pages**
   - Settings → Pages → Deploy from branch → `main` / `(root)`
2. **OAuth App**
   - Homepage: https://<your-username>.github.io/noobee-cms/
   - Callback: https://<your-username>.github.io/noobee-cms/admin/callback
   - Copy *Client ID* to `config.yml` under `app_id`.
3. **Edit `config.yml`**
   - repo: `<your-username>/noobee-cms`
   - public_folder: `/noobee-cms/uploads`

## Collections
- Blog → `content/blog`
- Resources → `content/resources`
- Accessibility Reviews → `content/reviews`

## Common issues
- Images 404 → update `public_folder` with `/noobee-cms/`
- GitHub login hangs → check OAuth callback URL
- YAML errors → use spaces, no tabs, no duplicate keys
