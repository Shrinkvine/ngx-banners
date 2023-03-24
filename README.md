# ngx-banners

ngx-banners is an angular component that allows you to create a banner with multiple options.

## Installation

```bash
npm i ngx-banners
```

## Usage
Import NgxBannerModule to your main module, for example, to app.module.ts:
```ts
   ...
   import { NgxBannerModule } from 'ngx-banners';
   ...
   
   @NgModule({
     ...
     imports: [
       ...
       NgxBannerModule,
       ...
     ],
     ...
   })
```
Using inside target component:
```html
<ngx-banner 
  [showBanner]="true" 
  [duration]="5000" 
  [bannerText]="My banner works!" 
  [buttonText]="Click Me!" 
  [onClick]="someCustomFunction"> 
</ngx-banner>
```
Properties and Defaults:
```ts
showBanner: boolean = false; // banner will only show when true
bannerText: string = ''; // text shown in the banner
buttonText: string = ''; // text shown in the button. will only show if onClick is defined
duration: number = 0; // if 0 it will show until user dismisses. duration in ms
onClick: (() => void) | null = null; // if onClick is null, the button will not show
```
## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)
