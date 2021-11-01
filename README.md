# Glide_Demo
Load images using Glide

![ss1](https://user-images.githubusercontent.com/57729176/139635360-616a5b0f-954c-46dc-9284-3c6e0d423a87.png)

## Image used
private val image = "https://cdn.pixabay.com/photo/2018/05/03/21/49/android-3372580_1280.png"

## Add Glide dependencies

    implementation 'com.github.bumptech.glide:glide:4.12.0'
    annotationProcessor 'com.github.bumptech.glide:compiler:4.12.0'
    
## Internet permession
<uses-permission android:name="android.permission.INTERNET"/>

## Code to load images
Glide.with(this)
            .load(image)
            .into(imageOne)
        Glide.with(this)
            .load(image)
            .fitCenter()
            .circleCrop()
            .diskCacheStrategy(DiskCacheStrategy.ALL)
            .placeholder(R.drawable.ic_launcher_background)
            .into(imageTwo)
