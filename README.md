# human-gait-data-acquisition-system 
Разработка программного обеспечения микроконтроллера ESP32 для специализированного устройства съёма данных походки человека.
Алгоритм работы предполагает считывание и передачу пакета данных, характеризующих перемещение нижних конечностей человека в пространстве за время осуществления различных активностей. Код для микроконтроллера выполняет задачи в два потока с использованием FreeRtos. На первом ядре осуществляется считывание данных с IMU датчиков с последующим размещением данных в общий контейнер памяти.Это необходимо для реализации поочередного взаимодействия ядер с одними и теми же данными так как на втором ядре разработан парсинг данных по протоколу TCP/IP и получение команд с дополнительного устройства. В данном случае, в качестве дополнитеьного устройства, предназначенного для сохранения и анализа данных, а так же для отслеживания качества калибровки датчиков и запуска парсинга данных выступает мобильное приложение, разработанное другим членом команды.
