ee-mysql
========

[![Greenkeeper badge](https://badges.greenkeeper.io/eventEmitter/ee-mysql.svg)](https://greenkeeper.io/)

mysql connector supporting transactions and pooling


	var MySQL = require( "ee-mysql" );

	var db = new MySQL( {
		  database: 		"dbName"
 		, hosts: [
 			{
		          host:     "1dbHsot"
		        , user:     "dbUser"
		        , password: "dbPass"
		        , weight: 	"optional int ( used for load balancing )"
		        , writable: true
		    }
		]
	} );


	db.query( "SELECT whatever FROM myDatabase WHERE id = ?;", [ id ], function( err, rows ){
		if ( err ) throw err;
		log.dir( rows );
	} );