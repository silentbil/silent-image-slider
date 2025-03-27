# Image slider card for Home Assistant

If you like my hard work and want to help with server cost, consider buying me a coffee :)<br>
<a href="https://www.buymeacoffee.com/silentbil" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>

## Demo
![demo](demo.gif)


## HACS Installation (Preferred option with updates)

TBD.

## HACS manual Installation
- In the HACS Frontend, click the 3 dots in the upper right
- Click 'Add Custom Repository'
- Fill in the repo url https://github.com/silentbil/silent-image-slider and choose 'Lovelace' category.
- Install the custom card (should now appear in the Frontend)
- HACS should automatically add the following to your resources:
```
url: /hacsfiles/silent-image-slider/silent-image-slider.js
type: Javascript Module
```

## Implementation

Images can be local or remote. If you are using local images, make sure to place them in the www folder of your Home Assistant configuration.

```
type: custom:silent-image-slider
speed: 3
images:
  - /local/car.jpeg
  - https://static.vecteezy.com/system/resources/previews/048/558/869/non_2x/cute-family-with-children-avatar-character-free-png.png
  - https://png.pngtree.com/png-vector/20240518/ourlarge/pngtree-beautiful-family-avatar-png-image_12476828.png
  - https://thumbs.dreamstime.com/b/family-avatar-cartoon-character-portrait-couple-man-glasses-carrying-child-over-shoulder-vector-illustration-graphic-149661660.jpg
```

### Options 
| Name        | Description               | Default | Required | Values           |
|-------------|---------------------------|---------|----------|------------------|
| `speed`     | slider speed              | 3       | No       | number 1-5       |
| `infinite`  | infinite slide            | Yes     | No       | boolean          |
| `showArrow` | Show next/prev arrows     | No      | No       | boolean          |
| `images`    | List of images to display | []      | Yes      | Array of strings |
