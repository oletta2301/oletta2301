from PIL import Image

def convert_to_16bit(input_image_path, output_image_path):
    # Открываем исходное изображение
    original_image = Image.open(input_image_path)

    # Переводим в 16-битный формат (оттенки серого)
    converted_image = original_image.convert('I;16')

    # Сохраняем сконвертированное изображение
    converted_image.save(output_image_path)

if __name__ == "__main__":
    # Укажите путь к исходному изображению и путь для сохранения 16-битного изображения
    input_image_path = "path_to_input_image.jpg"
    output_image_path = "path_to_output_image.tif"

    convert_to_16bit(input_image_path, output_image_path)
