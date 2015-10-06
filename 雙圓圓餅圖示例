$(function () {
    
        var colors = Highcharts.getOptions().colors,
            data = [{
                    y: 40,
                    color: colors[0],
                    drilldown: {
                        name: 'MSIE versions',
                        categories: ['Main 1'],
                        data: [55.11],
                        color: colors[0]
                    }
                }, {
                    y: 21,
                    color: colors[1],
                    drilldown: {
                        name: 'Firefox versions',
                        categories: ['Main 2'],
                        data: [21.63],
                        color: colors[1]
                    }
                }, {
                    y: 26,
                    color: colors[2],
                    drilldown: {
                        name: 'Chrome versions',
                        categories: ['Main 3'],
                        data: [11.94],
                        color: colors[2]
                    }
                }, {
                    y: 7,
                    color: colors[3],
                    drilldown: {
                        name: 'Safari versions',
                        categories: ['Main 4'],
                        data: [7.154],
                        color: colors[3]
                    }
                }, {
                    y: 7,
                    color: colors[4],
                    drilldown: {
                        name: 'Opera versions',
                        categories: ['Main 5'],
                        data: [ 2.14],
                        color: colors[4]
                    }
                }];
        // Build the data arrays
        var browserData = [];
        var versionsData = [];
        var myData=['<b>Liability Risk<br/>責任風險</b>','<b>Employee Benefit<br/>員工福利</b>','<b>Property Risk<br/>財產風險</b>','<b>Crime Risk<br/>犯罪風險</b>','<b>Financial Risk<br/>財務風險</b>'];
        var mytwoData=['Directors & Officers Liability (董監事責任保險)<br/>Commercial General LiabilityInsurance (商業綜合責任保險)<br/>Public Liability Insurance  (公共意外責任保險)<br/>Products Liability Insurance (產品責任保險)<br/>','Travel Insurance (旅行平安險)<br/>Health Insurance (健康保險)<br/>Term Life Insurance (定期壽險)<br/>','Property Damage Insurance (財產保險)<br/>Business Interruption Insurance (營業中斷保險)<br/>Marine Cargo Insurance (貨物運輸保險)<br/>Vehicle Insurance (汽車保險)<br/>Money Insurance (現金保險)<br/>','Crime Insurance (犯罪保險)<br/>Employee Fidelity Insurance (員工誠實保證保險)','Trade Credit Insurance (商業信用保險)'];
        for (var i = 0; i < myData.length; i++) {
    
            // add browser data
            browserData.push({
                name: myData[i],
                value:mytwoData[i],
                y: data[i].y,
                color: data[i].color
            });
            // add detail data
            versionsData.push({
                name: mytwoData[i],
                value:myData[i],
                y: data[i].y,
                color: data[i].color
            });
           
        }
    
        // Create the chart
        $('#container').highcharts({
            chart: {
                type: 'pie'
            },
            title: {
                text: 'Enterprise Risk and Insurance 企業風險與保險'
            },
            yAxis: {
                categories :mytwoData
            },
            plotOptions: {
                pie: {
                    shadow: false,
                    center: ['50%', '50%']
                }
            },
            tooltip: {
                pointFormat: '{point.key}'
            },
            series: [
                {
                name: 'Browsers',
                    data: ['我是中心'],//point key
                size: '20%',
                dataLabels: {
                    formatter: function() {
                        return  '<b>Enterprise Risk</b><br/><b>  and Insurance</b><br/><b>  企業風險與保險</b>';},
                    color: 'black',
                    distance: -25
                }
            },
                {
                name: 'Browsers',
                data: versionsData,//point key
                size: '100%',
                innerSize: '37%',  
                dataLabels: {
                    formatter: function() {
                        return  this.point.value;
                    },
                    color: 'black',
                    distance: 2
                }
            }]
        });
    });
    
