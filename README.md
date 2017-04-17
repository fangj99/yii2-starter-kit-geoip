# yii2-starter-kit-geoip
added two more functions to orignal yii2-geoip extension

## You can get all the files in this repository
### https://github.com/lysenkobv/yii2-geoip


## Added two more functions to get ip address's timezone and postal code in src/Result.php

```
    protected function getPostal($data) {
        $value = null;

        if (isset($data['postal']['code'])) {
            $value = $data['postal']['code'];
        }

        return $value;
    }


    protected function getTimezone($data) {
        $value = null;
        
        //\Yii::info('get post data', 'oauth');

        if (isset($data['location']['time_zone'])) {
            $value = $data['location']['time_zone'];
        }

        return $value;
    }


```

## You can add more functions by yourself according to the data structure listed below:

### http://dev.maxmind.com/geoip/geoip2/javascript/

### Sample Oject
```
{
  "city": {
    "geoname_id": 5368518,
    "names": {
      "en": "Los Gatos"
    }
  },
  "continent": {
    "code": "NA",
    "geoname_id": 6255149,
    "names": {
      "de": "Nordamerika",
      "en": "North America",
      "es": "Norteamérica",
      "fr": "Amérique du Nord",
      "ja": "北アメリカ",
      "pt-BR": "América do Norte",
      "ru": "Северная Америка",
      "zh-CN": "北美洲"
    }
  },
  "country": {
    "iso_code": "US",
    "geoname_id": 6252001,
    "names": {
      "de": "USA",
      "en": "United States",
      "es": "Estados Unidos",
      "fr": "États-Unis",
      "ja": "アメリカ合衆国",
      "pt-BR": "Estados Unidos",
      "ru": "США",
      "zh-CN": "美国"
    }
  },
  "location": {
    "accuracy_radius": 10,
    "latitude": 37.2266,
    "longitude": -121.9747,
    "metro_code": 807,
    "time_zone": "America/Los_Angeles"
  },
  "postal": {
    "code": "95030"
  },
  "registered_country": {
    "iso_code": "US",
    "geoname_id": 6252001,
    "names": {
      "zh-CN": "美国",
      "de": "USA",
      "en": "United States",
      "es": "Estados Unidos",
      "fr": "États-Unis",
      "ja": "アメリカ合衆国",
      "pt-BR": "Estados Unidos",
      "ru": "США"
    }
  },
  "subdivisions": [
    {
      "iso_code": "CA",
      "geoname_id": 5332921,
      "names": {
        "en": "California",
        "es": "California",
        "fr": "Californie",
        "ja": "カリフォルニア州",
        "pt-BR": "Califórnia",
        "ru": "Калифорния",
        "zh-CN": "加利福尼亚州",
        "de": "Kalifornien"
      }
    }
  ],
  "traits": {
    "autonomous_system_number": 7922,
    "autonomous_system_organization": "Comcast Cable Communications, LLC",
    "domain": "comcast.net",
    "isp": "Comcast Cable",
    "organization": "Comcast Cable",
    "ip_address": "67.180.128.246"
  },
  "represented_country": {
    "names": {}
  }
}
```

