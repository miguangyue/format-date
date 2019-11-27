# format-date
///Date(1574761002000)/
  function formatDate (date) {
     let  d = eval('new ' + date.substr(1, date.length - 2));
    let d_date = [d.getFullYear(), d.getMonth() + 1, d.getDate()];
    let d_time = [d.getHours(), d.getMinutes(), d.getSeconds()];
      return dFormat(d_date).join('-')+' '+ dFormat(d_time).join(':');
    }
    function dFormat(d_date) {
        d_date.map(s => {
            s = +s < 10 ? '0' + s : s; 
        });
        return d_date;
    }
