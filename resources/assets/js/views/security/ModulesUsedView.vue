
<style scoped>

	.link-space {
		padding-right: 40px;
	}
 
</style>

<template>

<div>
 	<mypopup slot="message"></mypopup>
	<myimport slot="modal-import" url-import="security/modules/import"></myimport>
	<mytopmenu show-menu="true"></mytopmenu> 
	<div class="container-fluid" >
		<div class="row" >
			<div class="col-sm-2">
				<mysubmenu submenu= "security"></mysubmenu>
			</div>
			<div class="col-sm-10" >
				<mymessage 
					message="dashboardTopMessage"
					color="info"
					align="center"
				>
				</mymessage>

				<myhorizontallinks name="horizontal-links"></myhorizontallinks>

				<div class="row" style="padding:0px">
					<div class="col-sm-12" style="padding:0px">
					 
					  <div style="padding-left:10px;padding-right:20px">
					  
					  	<mychart 
					  		id="Chart1"
					  		type="spline"
					  		width="500"
					  		height="250"
							url="/security/dashboard/modulesUsedByDay"
							title="modulesUsedByDay"
							x-title="Days"
							y-title="Modules Used"
							legend-position="bottom"
							legend-display="false"
							show-year="true"
							show-month="true"
					  	>

					  	</mychart>

					 	</div>
					</div>
				</div>
				
				<div class="row" style="padding:0px">
					<div class="col-sm-12" >
					 
						<mytableyearmonth  

							table-id="table1"

							table-title="modulesUsed" 

							columns-names='{
								"0": { "name": "moduleName", "width":"50%"},
								"1": { "name": "clicks" , "width":"50%"}
									
							}' 
							
							url="security/dashboard/modulesUsed"

							icon-info='{ }'

							icon-actions='{ }'

							show-year ="true"

							show-month = "true"

							>

							</mytableyearmonth>

						</div>
						
				</div>

				<div class="row" style="padding:0px">
					<div class="col-sm-12" style="padding:0px">
					 
					  <div style="padding-left:10px;padding-right:20px">
					  
					  	<mychart 
					  		id="Chart2"
					  		type="column"
					  		width="500"
					  		height="250"
							url="/security/dashboard/modulesUsedByMonth"
							title="modulesUsedByMonth"
							x-title="Days"
							y-title="Modules Used"
							legend-position="top"
							legend-display="false"
							show-year="true"
							show-month="false"
					  	>
					  	</mychart>

					 	</div>
					</div>
				</div>


			</div>		
		</div>		
	</div>
</div>
</template>


<script 

src="../../main.js" type="text/javascript">
	
</script>



										