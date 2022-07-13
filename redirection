 <?php 
 
 $actual_links = (isset($_SERVER['HTTPS']) && $_SERVER['HTTPS'] === 'on' ? "https" : "http") . "://$_SERVER[HTTP_HOST]$_SERVER[REQUEST_URI]";
 
    $getActualLink = explode('/',$actual_links);
    //print_r($getActualLink);
    $actual_link = "https://".$getActualLink[2].'/'.$getActualLink[3].'/'.$getActualLink[4].'/'.$getActualLink[5].'/';
    $spesQARR=mysql_query("Select * from mma_static_pages where Status='1'  order by DisOrder + 0 asc ");
     while($spedataArr=mysql_fetch_array($spesQARR))
    {
       $myArr[] = SITE_URL.$spedataArr['page_url'];
    }

    if(!in_array($actual_links,$myArr) ){
      //	header('Location:'. $actual_link,TRUE,301);
       	require('404.php');
    	die();
   }
   
   ?>
