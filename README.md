# bitmap_drawable_int
图片三种格式的相互转换

获取本地图片
Bitmap decodeResource = BitmapFactory.decodeResource(context.getResources(), R.drawable.img1);

把本地的int类型的图片转换成drawable
Drawable drawable = context.getResources().getDrawable(R.drawable.img1); 

把本地的int类型的图片转换成Bitmap 
Resources r = this.getContext().getResources();
Inputstream is = r.openRawResource(R.drawable.my_background_image);
BitmapDrawable  bmpDraw = new BitmapDrawable(is);
Bitmap bmp = bmpDraw.getBitmap();

Bitmap转Drawable 
Bitmap bm=xxx; //xxx根据你的情况获取 
BitmapDrawable bd=BitmapDrawable(bm); 
因为BtimapDrawable是Drawable的子类，最终直接使用bd对象即可。 

