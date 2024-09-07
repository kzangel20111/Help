# Help
Библиотека discord,flask,keras_model,import_model

  np.set_printoptions(suppress=True)
  model = load_model("/content/keras_model.h5", compile=False)
  class_names = open("labels.txt", "r").readlines()
  data = np.ndarray(shape=(1, 224, 224, 3), dtype=np.float32)


  image = Image.open("/content/images (29).jpg").convert("RGB")


  size = (224, 224)
  image = ImageOps.fit(image, size, Image.Resampling.LANCZOS)


  image_array = np.asarray(image)


  normalized_image_array = (image_array.astype(np.float32) / 127.5) - 1


  data[0] = normalized_image_array


  prediction = model.predict(data)
  index = np.argmax(prediction)
  class_name = class_names[index]
  confidence_score = prediction[0][index]

  return class_name[2:1]

path = files.upload()
path = list(path.keys())[0]
image=Image.open(path)


name = ecosortirovka(path)
if name == "trash":
  print("Это мусор мусор очень опасен для природы пожалуеста не выкидывайте мусор куда попало")
  print("Лучше посмотрите вниз там есть пример куда нужно выбросить мусор")
if name ==("paper"):
  print("Это бумага бумага вредит природе после использования бумаги пожалуйста Не выкидывай его куда попало")
  print("Лучше посмотрите вниз там есть пример куда нужно выбросить бумагу")
if name ==("plastic"):
  print("пластик тоже опасен для природы например разлагается пластик примерно 450-500 лет. В течение этого времени пластик выделяет много токсичных элементов, которые отравляют почву, воду и воздух, попадают в пищу животных, птиц и рыб, убивая их, наносят непоправимый ущерб природе.")
  print("Лучше посмотрите вниз там есть пример куда нужно выбросить стекло")
if name == ("metal"):
  print("Металл тоже опасен для природы в нее входет токсичные елементы которые вредят жывотным и даже людям")
  print("Лучше посмотрите вниз там есть пример куда нужно выбросить металл")
