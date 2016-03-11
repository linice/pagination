# pagination
Pagination contains an instantiable class, along with a view which renders the pagination markup.

The purpose of this library is to provide a simple API to render pagination markup, without having to worry about including common files and set too many settings. With this class, you simply pass in your parameters and make a call to the instance's *<parse> method.

Pagination using bootstrap theme(css), so just include bootstrap.css in your view page.


` php <?php
// source inclusion
require_once PRJ_PATH . '/vendor/pagination/Pagination.class.php';

use Pagination;


// determine page (based on <_GET>)
$page = isset($_GET['page']) ? ((int) $_GET['page']) : 1;
// instantiate; set current page; set number of records
$pagination = new Pagination();
$pagination->setCurrent($page);
$pagination->setRPP(15);
$pagination->setTotal(200);
// grab rendered/parsed pagination markup
$pager = $pagination->parse();

`
