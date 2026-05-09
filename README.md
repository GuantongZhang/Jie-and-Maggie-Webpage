# Listing Management

All property listings are managed inside:

    script.js

Locate the section:

    var listingsData = [

Each listing is represented as an object inside this array.

---

## Add a Listing

Copy an existing listing object and update the values.

Example:

    {
        image: 'assets/example.jpg',
        title: '123 Example St',
        address: 'Irvine, CA 92618',
        stats: '4 Beds · 3 Baths · 2,500 sqft',
        price: '$1,800,000',
        status: 'listing'
    }

Fields:

- `image`
  Path to image file.

- `title`

- `address`

- `stats`

- `price`

- `status`
  Supported values:
  
      listing
      in escrow
      sold

---

## Delete a Listing

Remove the entire object from the `listingsData` array.
Be careful to preserve commas between remaining objects.

---

## Replace / Add Images

Listing images are stored in:

    /assets/

Steps:

1. Upload the new image into the `assets` folder.
2. Update the `image` field in the listing object.

Example:

    image: 'assets/new-property.jpg'

Recommended:

- JPG, JPEG or PNG
- Landscape orientation
- Compressed image size for faster loading

---

## Publish Changes

After editing:

1. Save changes.
2. Commit changes to the repository.
3. Push to the production branch.

Example:

    git add .
    git commit -m "Update listings"
    git push

Cloudflare Pages will automatically detect the new commit and redeploy the site.
