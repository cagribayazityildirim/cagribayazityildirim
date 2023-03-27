Pytest, bir Python test çerçevesidir ve test fonksiyonlarının yanı sıra özellikle pytest modülünde tanımlanmış bir dizi decorator (süsleyici) sağlar. Bu decorator'lar testlerin davranışını değiştirir, test sonuçlarını filtreler ve hatta test sonuçlarının raporlanmasını özelleştirmenize yardımcı olur.

@pytest.fixture: Bir testin kullanabileceği önceden tanımlanmış bir nesne veya değer sağlar. Örneğin, bir test veritabanıyla etkileşim kuruyorsa, bir fixture, veritabanı bağlantısını açar, test etkinliği sırasında kullanılan verileri doldurur ve testin tamamlanmasından sonra veritabanı bağlantısını kapatır.

@pytest.mark.parametrize: Test fonksiyonlarının birden fazla kez çalıştırılmasını sağlar ve farklı parametrelerle çalıştırılarak testin davranışını kontrol etmenize olanak tanır. Bu, test fonksiyonunun kendisini birkaç kez tekrarlamak yerine, farklı argümanlarla birçok kez çağırılması ile yapılır.

@pytest.mark.parametrize("arg1, arg2", [(1, 2), (3, 4), (5, 6)]): Bu, test fonksiyonuna "arg1" ve "arg2" argümanlarını sağlar ve bu argümanların sırayla 1 ve 2, 3 ve 4, 5 ve 6 olarak atandığını gösterir.

@pytest.mark.parametrize("num", [1, 2, 3], ids=["one", "two", "three"]): Bu, test fonksiyonuna "num" argümanını sağlar ve bu argümanın sırayla 1, 2, 3 olarak atandığını gösterir. Ayrıca, her argümanın id'sini ("one", "two", "three") de sağlar.

@pytest.mark.parametrize("num", [1, 2, 3], indirect=True): Bu, test fonksiyonuna "num" adında bir argüman sağlar ve bu argümanın sırayla 1, 2, 3 olarak atandığını gösterir. Ayrıca, argümanın değerini bir fixture'dan almış olduğunu belirtir.

@pytest.mark.parametrize("name, value", [("num1", 1), ("num2", 2)]): Bu, test fonksiyonuna "name" ve "value" argümanlarını sağlar ve bu argümanların sırayla "num1" ve 1, "num2" ve 2 olarak atandığını gösterir.

@pytest.mark.skip: Belirli bir testin atlanmasını sağlar. Örneğin, belirli bir testin belirli bir koşul altında çalıştırılmasının uygun olmadığı durumlarda bu kullanılabilir.

@pytest.mark.xfail: Testin başarısız olmasını beklediğiniz ve bunun bir hata olarak raporlanmamasını istediğiniz durumlarda kullanılır. Bu, bir hata yerine bir uyarı olarak raporlanır.

@pytest.mark.timeout: Testin belirli bir süre içinde tamamlanmasını sağlar. Eğer test bu süre içinde tamamlanamazsa, hata olarak raporlanır.

@pytest.mark.filterwarnings: Testin belirli bir uyarı mesajını atlamasını sağlar. Örneğin, belirli bir uyarı mesajının görüntülenmesini istemediğiniz durumlarda kullanılabilir.

@pytest.mark.slow: Testin uzun süre çalıştığını belirtmek için kullanılır. Bu, test süresinin uzun olduğu durumlarda, testlerin daha verimli bir şekilde planlanmasını sağlamaya yardımcı olur.
