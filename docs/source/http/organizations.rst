organizations
=============

Метод возвращает все организации, к которым у пользователя есть доступ.

**GET <endpoint>/v2/organizations**


Пример запроса:

::

  GET /v2/organizations HTTP/1.1
  Host: ofd-project.kontur.ru:11002
  Cache-Control: no-cache
  ofd_api_key=031c1120-9hhe-435e-5h08-43091hhcd71d;auth.sid=FEC4454C200EC54BJ7GE4PO0011121C4E7E79C795HHTG395JD16C002EG125CFA;


В теле ответа возвращаются организации с их реквизитами в виде массива JSON-объектов следующей структуры:

::

  [
    {
      "id": "",           //идентификатор организации
      "inn": "",          //ИНН
      "ogrn": "",         //ОРГН
      "shortName": "",    //краткое наименование
      "fullName": ""      //полное наименование
    }
  ]


Пример ответа:

::

  [
    {
      "id": "c2e3a34c-823f-4b1e-a9g1-d94fa40c22a6",
      "inn": "6699000000",
      "ogrn": "000000000000000",
      "shortName": "ООО Тестовая организация",
      "fullName": "Общество с органиченной ответственностью Тестовая организация"
    }
  ]


Для получения реквизитов организации по её идентификатору, используйте метод :doc:`organization`
