-----------------SASS----------------------
Sass bir css yazma yöntemidir.Dosya uzantısı .scss'dir.
Browserlar scss dosyalarını okuyamadığı için node-sass karşımıza bir çözüm olarak çıkar ve bu çözüm .scss dosyalarını css dosyalarına yani browserların okuyabileceği formata çevirir.

Yüklemek İçin
-npm init -y
-npm install node-sass

Örnek package.json dosyası
{
"name": "sass",
"version": "1.0.0",
"description": "",
"main": "index.js",
"scripts": {
"sass": "node-sass -w scss/ -o dist/css/ --recursive"
},
"keywords": [],
"author": "",
"license": "ISC",
"dependencies": {
"node-sass": "^8.0.0"
}
}

scss klasörünün içindeki dosyalarda ismi "\_variables.scss" olan
dosyalar görürüz.Bu dosyalar import işlemi veya main scss dosyamızı karmaşıklıktan uzak tutmak amacıyla kullanılan partial css dosyalardır.Bu sebeple node-sass tarafından "package.json" dosyasında belirtilen main.css dosyasının yanına yeni bir css dosyası oluşturulmaz.
