## CSS not loading for Admin when DEBUG = False

```Python
STATIC_URL = '/static/'  # URL prefix for static files (e.g., CSS, JavaScript, images)
STATICFILES_DIRS = [os.path.join(BASE_DIR, 'static')]
STATIC_ROOT = os.path.join(BASE_DIR, 'static_files/')

MEDIA_URL = '/media/'

# Define the directory where uploaded media files are stored
MEDIA_ROOT = BASE_DIR / 'media'

```

pip install whitenoise

```Python
# settings.py
MIDDLEWARE = [
    # ... your other middleware ...
    'whitenoise.middleware.WhiteNoiseMiddleware',
]


```