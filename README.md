Parche de A03 Injection

El parche consiste en hacer una verificación de la extensión que se está enviando en el JSON, se verifica que sea PNG o JPEG o JPG si es así si guarda la imagen, de lo contrario no la guarda y muestra un R:-5, con esa verificación se obliga a que se suba una imagen y no un archivo

index.php Código agregado:

// Valida que la extension del archivo sea png o jpg o jpeg, No diferencia entre mayúsculas y minúsculas
if (!(strcasecmp($jsB['ext'], "PNG") == 0 || strcasecmp($jsB['ext'], "JPG") == 0  || strcasecmp($jsB['ext'], "JPEG") == 0)) {
  echo '{"R":-5}';
  return;
}
