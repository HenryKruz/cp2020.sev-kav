<template>
    <div>
        <app-header></app-header>
        <div class="left-side-block">
            <div class="accordion" id="accordion">
                <div class="card">
                    <div class="card-header" id="substation">
                        <h5 class="mb-0">
                            <button class="btn btn-link" type="button" data-toggle="collapse" data-target="#collapseSubstation" aria-expanded="false" aria-controls="collapseSubstation">
                                Подстанции
                            </button>
                        </h5>
                    </div>
                    <div id="collapseSubstation" class="collapse" aria-labelledby="substation" data-parent="#accordion">
                        <div class="card-body">
                            <ul>
                                <li v-for="station in dataStations" :key="station.name">{{station.name}}</li>
                            </ul>
                        </div>
                    </div>
                </div>
                <div class="card">
                    <div class="card-header" id="lines">
                        <h5 class="mb-0">
                            <button class="btn btn-link" type="button" data-toggle="collapse" data-target="#collapseLines" aria-expanded="false" aria-controls="collapseLines">
                                Линии ЛЭП
                            </button>
                        </h5>
                    </div>
                    <div id="collapseLines" class="collapse" aria-labelledby="lines" data-parent="#accordion">
                        <div class="card-body">
                            <ul>
                                <li>Линия 235654</li>
                                <li>Линия 235655</li>
                                <li>Линия 235656</li>
                                <li>Линия 235657</li>
                                <li>Линия 235658</li>
                                <li>Линия 235659</li>
                                <li>Линия 235660</li>
                                <li>Линия 235661</li>
                                <li>Линия 235662</li>
                                <li>Линия 235663</li>
                                <li>Линия 235664</li>
                                <li>Линия 235665</li>
                                <li>Линия 235666</li>
                                <li>Линия 235667</li>
                                <li>Линия 235668</li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div id="map" class="map">
            <!--<iframe src="http://yandex.ru/map-widget/v1/?um=constructor%3Aa02ac7f52d0f38c49523506839cd4a9f51315128569b2d6a05b6e432d84c28f7&amp;source=constructor" width="617" height="457" frameborder="0"></iframe>-->
        </div>
        <div class="right-side-block">
            <div class="card">
                <div class="card-header" id="accidents">
                    <h5 class="mb-0">
                        <button class="btn btn-link" type="button" data-toggle="collapse" data-target="#collapseAccidents" aria-expanded="false" aria-controls="collapseAccidents">
                            Аварии
                        </button>
                    </h5>
                </div>
                <div id="collapseAccidents" class="collapse" aria-labelledby="accidents" data-parent="#accordion">
                    <div class="card-body">
                        <div class="accordion" id="accordionAccidents">
                            <div class="card">
                                <div class="card-header" id="accidents1">
                                    <h6 class="mb-0">
                                        <button class="btn btn-link" type="button" data-toggle="collapse" data-target="#collapseAccidents1" aria-expanded="false" aria-controls="collapseAccidents1">
                                            <span style="color: red">20 октября 2020, 23:14</span>
                                        </button>
                                    </h6>
                                </div>
                                <div id="collapseAccidents1" class="collapse" aria-labelledby="accidents1" data-parent="#accordion">
                                    <div class="card-body">
                                        <span><strong>Линия 2354</strong></span>
                                        <table>
                                            <tr>
                                                <td>Тип КЗ</td>
                                                <td>Фаза А на землю</td>
                                            </tr>
                                            <tr>
                                                <td>Причина</td>
                                                <td>Обрыв</td>
                                            </tr>
                                            <tr>
                                                <td>Длительность</td>
                                                <td>0,25 сек</td>
                                            </tr>
                                            <tr>
                                                <td>АПВ</td>
                                                <td><span style="color: red">Неуспешное</span></td>
                                            </tr>
                                            <tr>
                                                <td>Расстояние</td>
                                                <td>452 м; 980 м</td>
                                            </tr>
                                        </table>
                                        <span><a href="#" class="btn btn-danger">Вызвать бригаду</a></span>
                                        <span><a href="http://stavteam2020.ddns.net:5000/graph/1" target="_blank" class="btn btn-light">Осцилограмма</a></span>
                                    </div>
                                </div>
                            </div>
                            <div class="card">
                                <div class="card-header" id="accidents2">
                                    <h6 class="mb-0">
                                        <button class="btn btn-link" type="button" data-toggle="collapse" data-target="#collapseAccidents2" aria-expanded="false" aria-controls="collapseAccidents2">
                                            <span>19 октября 2020, 10:58</span>
                                        </button>
                                    </h6>
                                </div>
                                <div id="collapseAccidents2" class="collapse" aria-labelledby="accidents2" data-parent="#accordion">
                                    <div class="card-body">
                                        <span><strong>Линия 2358</strong></span>
                                        <table>
                                            <tr>
                                                <td>Тип КЗ</td>
                                                <td>Фаза B на землю</td>
                                            </tr>
                                            <tr>
                                                <td>Причина</td>
                                                <td>Обрыв</td>
                                            </tr>
                                            <tr>
                                                <td>Длительность</td>
                                                <td>0,25 сек</td>
                                            </tr>
                                            <tr>
                                                <td>АПВ</td>
                                                <td><span style="color: green">Успешное</span></td>
                                            </tr>
                                            <tr>
                                                <td>Расстояние</td>
                                                <td>320 м; 1580 м</td>
                                            </tr>
                                        </table>
                                        <span><a href="http://stavteam2020.ddns.net:5000/graph/1" target="_blank" class="btn btn-light">Осцилограмма</a></span>
                                    </div>
                                </div>
                            </div>
                            <div class="card">
                                <div class="card-header" id="accidents3">
                                    <h6 class="mb-0">
                                        <button class="btn btn-link" type="button" data-toggle="collapse" data-target="#collapseAccidents3" aria-expanded="false" aria-controls="collapseAccidents3">
                                            <span>16 октября 2020, 14:12</span>
                                        </button>
                                    </h6>
                                </div>
                                <div id="collapseAccidents3" class="collapse" aria-labelledby="accidents3" data-parent="#accordion">
                                    <div class="card-body">
                                        <span><strong>Линия 2362</strong></span>
                                        <table>
                                            <tr>
                                                <td>Тип КЗ</td>
                                                <td>Фаза A на землю</td>
                                            </tr>
                                            <tr>
                                                <td>Причина</td>
                                                <td>Обрыв</td>
                                            </tr>
                                            <tr>
                                                <td>Длительность</td>
                                                <td>0,25 сек</td>
                                            </tr>
                                            <tr>
                                                <td>АПВ</td>
                                                <td><span style="color: green">Успешное</span></td>
                                            </tr>
                                            <tr>
                                                <td>Расстояние</td>
                                                <td>412 м; 1208 м</td>
                                            </tr>
                                        </table>
                                        <span><a href="http://stavteam2020.ddns.net:5000/graph/1" target="_blank" class="btn btn-light">Осцилограмма</a></span>
                                    </div>
                                </div>
                            </div>
                            <div class="card">
                                <div class="card-header" id="accidents4">
                                    <h6 class="mb-0">
                                        <button class="btn btn-link" type="button" data-toggle="collapse" data-target="#collapseAccidents4" aria-expanded="false" aria-controls="collapseAccidents4">
                                            <span>16 октября 2020, 14:08</span>
                                        </button>
                                    </h6>
                                </div>
                                <div id="collapseAccidents4" class="collapse" aria-labelledby="accidents4" data-parent="#accordion">
                                    <div class="card-body">
                                        <span><strong>Линия 2322</strong></span>
                                        <table>
                                            <tr>
                                                <td>Тип КЗ</td>
                                                <td>Фаза A на землю</td>
                                            </tr>
                                            <tr>
                                                <td>Причина</td>
                                                <td>Обрыв</td>
                                            </tr>
                                            <tr>
                                                <td>Длительность</td>
                                                <td>0,18 сек</td>
                                            </tr>
                                            <tr>
                                                <td>АПВ</td>
                                                <td><span style="color: green">Успешное</span></td>
                                            </tr>
                                            <tr>
                                                <td>Расстояние</td>
                                                <td>603 м; 1015 м</td>
                                            </tr>
                                        </table>
                                        <span><a href="http://stavteam2020.ddns.net:5000/graph/1" target="_blank" class="btn btn-light">Осцилограмма</a></span>
                                    </div>
                                </div>
                            </div>
                            <div class="card">
                                <div class="card-header" id="accidents5">
                                    <h6 class="mb-0">
                                        <button class="btn btn-link" type="button" data-toggle="collapse" data-target="#collapseAccidents5" aria-expanded="false" aria-controls="collapseAccidents5">
                                            <span style="color:red">12 октября 2020, 20:20</span>
                                        </button>
                                    </h6>
                                </div>
                                <div id="collapseAccidents5" class="collapse" aria-labelledby="accidents5" data-parent="#accordion">
                                    <div class="card-body">
                                        <span><strong>Линия 2321</strong></span>
                                        <table>
                                            <tr>
                                                <td>Тип КЗ</td>
                                                <td>Фаза B на землю</td>
                                            </tr>
                                            <tr>
                                                <td>Причина</td>
                                                <td>Обрыв</td>
                                            </tr>
                                            <tr>
                                                <td>Длительность</td>
                                                <td>0,18 сек</td>
                                            </tr>
                                            <tr>
                                                <td>АПВ</td>
                                                <td><span style="color: red">Неуспешное</span></td>
                                            </tr>
                                            <tr>
                                                <td>Расстояние</td>
                                                <td>721 м; 918 м</td>
                                            </tr>
                                        </table>
                                        <span><a href="#" class="btn btn-danger">Вызвать бригаду</a></span>
                                        <span><a href="http://stavteam2020.ddns.net:5000/graph/1" target="_blank" class="btn btn-light">Осцилограмма</a></span>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import AppHeader from './main/Header.vue';
export default {
    data() {
        return {
            dataStations: {},
            dataLines: {}
        }
    },
    components: {
        AppHeader
    },
    methods: {

    },
    mounted() {
        let station = {}
        let lines = {}

        let data = {
            session: sessionStorage.getItem('sessionId')
        };

        axios.post('/map', data)
        .then(Response => (
            station = Response.data.stations,
            this.dataStations = station,
            lines = Response.data.lines,
            this.dataLines = lines,
            Object.entries(Response.data.stations).forEach(([key, value]) => {
                console.log(`${key} ${value.name}`);
            }),
            Object.entries(Response.data.lines).forEach(([key, value]) => {
                console.log(`${key} ${value.coordInStation.lat}`);
            })
        ))
        .catch(error => (
            false
        ));

        ymaps.ready(function () {
            var myMap = new ymaps.Map('map', {
                    center: [44.039795, 43.070634],
                    zoom: 9,
                    controls: ['default']
                }, {
                    searchControlProvider: 'yandex#search'
                }),

                // Создаём макет содержимого.
                MyIconContentLayout = ymaps.templateLayoutFactory.createClass(
                    '<div style="color: #FFFFFF; font-weight: bold;">$[properties.iconContent]</div>'
                );

                Object.entries(station).forEach(([key, value]) => {
                    myMap.geoObjects
                    .add(new ymaps.Placemark([value.lon, value.lat], {
                        hintContent: value.name,
                        balloonContent: ''
                    }, {
                        // Опции.
                        // Необходимо указать данный тип макета.
                        iconLayout: 'default#image',
                        // Своё изображение иконки метки.
                        iconImageHref: '/static/img/station_danger.png',
                        // Размеры метки.
                        iconImageSize: [30, 42]
                    }));
                });

                Object.entries(lines).forEach(([key, value]) => {
                    myMap.geoObjects
                    .add(new ymaps.GeoObject({
                        // Описываем геометрию геообъекта.
                        geometry: {
                            // Тип геометрии - "Ломаная линия".
                            type: "LineString",
                            // Указываем координаты вершин ломаной.
                            coordinates: [
                                [value.coordInStation.lon, value.coordInStation.lat],
                                [value.coordOutStation.lon, value.coordOutStation.lat]
                            ]
                        },
                        // Описываем свойства геообъекта.
                        properties:{
                            hintContent: "",
                            balloonContent: ""
                        }
                    }, {
                        // Задаем опции геообъекта.
                        // Включаем возможность перетаскивания ломаной.
                        draggable: false,
                        // Цвет линии.
                        strokeColor: "#FF0000",
                        // Ширина линии.
                        strokeWidth: 2
                    }));
                });
                
                myMap.controls.add('zoomControl');
        });
    }
}
</script>

<style scoped>
.left-side-block, .right-side-block {
    display: inline-block;
    position: absolute;
    width: 25%;
    height: 100%;
    padding-top: 6px;
}
.map {
    position: absolute;
    left: 25%;
    width: 50%;
    height: 100%;
    padding-top: 6px;
}
.left-side-block {
    float: left;
}
.right-side-block {
    right: 0;
}
.card-body .btn {
    font-size: 12px;
}
</style>