# Deploy JioSaavn API to Railway

## Quick Deploy Steps

1. **Create Railway Account**
   - Go to [railway.app](https://railway.app)
   - Sign up with GitHub

2. **Deploy from GitHub**
   - Click "New Project"
   - Select "Deploy from GitHub repo"
   - Choose your repository
   - Select the `jiosaavn-api` folder

3. **Configuration**
   Railway will automatically detect the Python app and use these settings:
   - **Build Command**: `pip install -r requirements.txt`
   - **Start Command**: `python app.py`
   - **Port**: 5100 (automatically detected)

4. **Environment Variables**
   No environment variables needed - the API works out of the box!

5. **Custom Domain** (Optional)
   - Go to Settings > Domains
   - Add a custom domain or use the provided railway.app subdomain

## Alternative: Manual Deployment

If you prefer manual deployment:

```bash
# Install Railway CLI
npm install -g @railway/cli

# Login to Railway
railway login

# Deploy from jiosaavn-api directory
cd jiosaavn-api
railway deploy
```

## Expected Deployment URL
After deployment, you'll get a URL like:
`https://your-app-name.railway.app`

## Test Your Deployment
```bash
# Replace with your actual Railway URL
curl "https://your-app-name.railway.app/result/?query=alone"
```

## Deployment Status
- ✅ No build configuration needed
- ✅ Automatic Python detection
- ✅ CORS already configured
- ✅ No environment variables required
- ✅ Scales automatically