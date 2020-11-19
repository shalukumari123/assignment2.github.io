<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link href="https://maxcdn.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css" rel="stylesheet" id="bootstrap-css">
    <style>
            .register .nav-tabs .nav-link:hover{
                border: none;
            }
            .text-align{
                margin-top: -3%;
                margin-bottom: -9%;

                padding: 10%;
                margin-left: 30%;
            }
            .form-new{
                margin-right: 22%;
                margin-left: 20%;
            }
            .register-heading{
                margin-left: 21%;
                margin-bottom: 10%;
                color: #e9ecef;
            }
            .register-heading h1{
                margin-left: 21%;
                margin-bottom: 10%;
                color: #e9ecef;
            }
            .register{
                background: -webkit-linear-gradient(left, #5f080d, #ff0000);
                margin-top: 3%;
                padding: 3%;
                border-radius: 2.5rem;
            }
            .btnSubmit
            {
                width: 50%;
                border-radius: 1rem;
                padding: 1.5%;
                color: #fff;
                background-color: #1e0a68;
                border: none;
                cursor: pointer;
                margin-right: 6%;
                color: rgb(246, 246, 252);
                margin-top: 4%;
            }
    </style>

</head>
<body>
    
<div class="container register">
            <div class="row">
                <div class="col-md-12">
                        <div class="tab-pane fade show active text-align form-new" id="home" role="tabpanel" aria-labelledby="home-tab">
                            <h3 class="register-heading">Form</h3>
                            <div class="row register-form">
                                <div class="col-md-12">
                                    <form method="post" autocomplete="off" name="google-sheet">
                                        <div class="form-group">
                                            <input type="text" name="Name" class="form-control" placeholder="Your Name " value="" required=""/>
                                        </div>
                                        <div class="form-group">
                                            <input type="date" name="DOB" class="form-control" placeholder="Your DOB " value="" required=""/>
                                        </div>
                                        <div class="form-group">
                                            <input type="number" name="Salary" class="form-control" placeholder="Your Salary " value="" required=""/>
                                        </div>
                                        <div class="form-group">
                                            <input type="submit" name="submit" class="btnSubmit btn-block" value="Login" />
                                        </div>
                                    </form>
                                    
                                 
                                    <button onclick="window.location.href='https://docs.google.com/spreadsheets/d/1rokDJbQpGwT-Etvuq6N5RjnTftjYXdYv_W8mrLbwvZU/export?format=xlsx';">
                                        Download
                                      </button><br>
                                      <button onclick="window.location.href='';">
                                        Upload
                                      </button><br>
                                      <iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vSAL6VdgmmCvH5yg_kJYZuQs2bs96KrgdLn9BRG9W9Of6Csqw_3EvrYS-6rRoMIbwXt5dEvhjwRxdda/pubhtml?gid=0&amp;single=true&amp;widget=true&amp;headers=false"></iframe>
                                  
                                 
                                
                                </div>
                            </div>
                        </div>
                </div>
            </div>
        </div>
          
          <script>
            const scriptURL = 'https://script.google.com/macros/s/AKfycbzI2XtQY65SMq2NbcwTRlMu97U2UfSMwno293mX2tIDOLFely8/exec'
            const form = document.forms['google-sheet']
          
            form.addEventListener('submit', e => {
              e.preventDefault()
              fetch(scriptURL, { method: 'POST', body: new FormData(form)})
                .then(response => alert("Thanks for filling this form.......Your information is stored in our excel database."))
                .catch(error => console.error('Error!', error.message))
            })
          </script>

        <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.1.1/js/bootstrap.min.js"></script>
        <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>

        
</body>
</html>
