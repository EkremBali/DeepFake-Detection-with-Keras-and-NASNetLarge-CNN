# DeepFake Detection with Keras and NASNetLarge CNN
 NASNetLarge CNN ve Keras ile DeepFake görüntünün algılanması.
 
 ![Model Resmi](https://github.com/EkremBali/DeepFake-Detection-with-Keras-and-NASNetLarge-CNN/blob/main/images/NASNetModel.JPG)
 
 Bu proje kapsamında görüntü sınıflandırma konusundaki başarısını ImageNet veri kümesinde kanıtlamış olan NASNetLarge CNN modeli DeepFake algılamada kullanılmış ve yüksek başarı elde edilmiştir. Donanım yetersizliğinden ötürü Celeb-DFv2 veri kümesinin tamamı kullanılamamış fakat bu şekilde de 0.967 accuracy elde edilmiştir.
 
 Within the scope of this project, the NASNetLarge CNN model, which has proven its success in image classification in the ImageNet dataset, has been used in DeepFake detection and has achieved high success. Due to hardware inadequacy, the entire Celeb-DFv2 dataset could not be used, but 0.967 accuracy was obtained in this way.
 
 Öncelikle veri kümesinden yüz bölgeleri çıkartılarak train, validation, test  için sırasıyla  aşağıdaki görselde görünen sayıda veri elde edilmiştir.
 
 First of all, facial regions were removed from the data set and the number of data shown in the image below was obtained for train, validation and testing, respectively.
 
 ![Veri Sayıları](https://github.com/EkremBali/DeepFake-Detection-with-Keras-and-NASNetLarge-CNN/blob/main/images/NAS4-veriSay%C4%B1s%C4%B1.JPG)
 
 Ardından oluşturulan bu veri kümesi üzerinde veri büyütme (image augmentation) teknikleri kullanılarak eğitim aşamasında aşırı öğrenme (overfitting) olması durumu önlenmiştir. Veriler bu şekilde hazır hale geldikten sonra NASNetLarge modeli katmanları tekrar eğitilebilir yapılmış ve bir adet yeni sınıflandırıcı katman eklenmiştir. Bu model eğitilmiş ve eğitim sonucunda yüksek başarı elde edilmiştir. Eğitim 12 epoch sürmüş fakat en iyi sonuç 9. epoch'da kaydedilmiştir.
 
 Then, by using image augmentation techniques on this data set, overfitting in the training phase was prevented. After the data is ready in this way, NASNetLarge model layers are made trainable again and a new classifier layer is added. This model has been trained and high success has been achieved as a result of the training. The training took 12 epochs, but the best result was recorded at the 9th epoch.
 
 ![Acc Grafik](https://github.com/EkremBali/DeepFake-Detection-with-Keras-and-NASNetLarge-CNN/blob/main/images/NAS4-AccuracyGraph.JPG)
 ![Loss Grafik](https://github.com/EkremBali/DeepFake-Detection-with-Keras-and-NASNetLarge-CNN/blob/main/images/NAS4-LossGraph.JPG)
 
 Son olarak elde edilen model test verileri üzerinde tahmin (predict) işlemine tabi tutulmuştur. Yapılan tahmin işlemlerinin %93'ü başarılı gerçekleşmiştir.
 
 Finally, the obtained model was predicted on the test data. 93% of the estimation processes were successful.
 
 ![Tahmin işlemi](https://github.com/EkremBali/DeepFake-Detection-with-Keras-and-NASNetLarge-CNN/blob/main/images/NAS4-TestVerileriY%C3%BCzdesi.JPG)
 
 Model hakkında daha detaylı bilgi için teknik makaleyi okuyabilirsiniz.
 
 For more detailed information about the model, you can read the technical article.
 
 ![Görüntü üzerinde tahmin](https://github.com/EkremBali/DeepFake-Detection-with-Keras-and-NASNetLarge-CNN/blob/main/images/gercek_Sahte_test.JPG)
