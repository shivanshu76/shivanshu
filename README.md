
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no" />
    <title>Download Admit Card - shivanshu</title>
    <link rel="stylesheet" href="style.css">
    <link rel="icon" type="image/x-icon" href="../img/aayansh_singh.gif" />
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" />
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
    <style>
        .btn-lg {
            padding: 12px 26px;
            font-size: 14px;
            font-weight: 700;
            letter-spacing: 1px;
            text-transform: uppercase;
        }

        ::placeholder {
            font-size: 14px;
            letter-spacing: 0.5px;
        }

        .form-control-lg {
            font-size: 16px;
            padding: 10px 20px;
        }

        .font-500 {
            font-weight: 500;
        }

        #overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            background-color: #000;
            filter: alpha(opacity=70);
            -moz-opacity: 0.7;
            -khtml-opacity: 0.7;
            opacity: 0.7;
            z-index: 100;
            display: none;
        }

        .popup {
            position: fixed;
            display: none;
            background-color: white;
            min-width: 320px;
            z-index: 101;
            top: 50%;
            left: 50%;
            padding: 20px;
            border-radius: 14px;
            transform: translate(-50%, -50%);
        }
    </style>
</head>

<body id="page-top">
    <div id="loader" class="center"></div>
    <div class="container">
        <div class="row mt-5">
            <div class="col-lg-6 col-12 mx-auto">
                <div class="p-4 bg-white rounded shadow-lg">
                    <h3 class="mb-2 text-center text-primary">Admit Card</h3>
                    <p class="text-center lead mx-4 text-black-50">Download Admit Card of bteup exam</p>

                    <label class="font-500">Enrollment No.</label>
                    <input id="enroll" name="enroll" class="form-control form-control-lg mb-3" type="text" required
                        maxlength="15">
                    <a id="download_admitcard"> <button
                            class="btn btn-primary btn-lg w-100 shadow-lg mt-4">Download</button></a>

                </div>
            </div>
        </div>

    </div>

    <section id="about" style="background-color: rgb(31, 60, 80); margin-top: 40px;">
        <div class="container py-5">
            <div class="row mt-4">
                <div class="col-lg-4 mx-auto text-center">
                    <img style="max-height:320px" src="https://drive.google.com/file/d/1w9xKetxEHUpGlwc_0RKUTY3h2ND79_jw/view?usp=sharing" class="img-fluid rounded-circle"
                        alt="shivanshu" />
                </div>
                <div class="col-lg-8 mx-auto ">
                    <h2 class="display-5 text-center mt-4" style="color:#bba990;font-weight:700;">Shivanshu
                       </h2>
                    <p class="lead text-white-50 text-center display-6">Programmer</p>
                    <p class="lead text-white-50 text-center mt-5">Sorry I do not want to talk about myself.</p>
                    <div class="social-btns text-center mt-5">
                        <a class="btn instagram" href="https://www.instagram.com/shivanshu_raikwar76/"><i
                                class="fa fa-instagram"></i></a>
                        <a class="btn facebook" href="https://www.facebook.com/shivanshu.raikwar.92"><i
                                class="fa fa-facebook"></i></a>
                        
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <section class="section-team" style="background-color: rgb(24, 48, 65);">
        <div class="container">
            <div class="row justify-content-center">
                <div class="col-md-8 col-lg-6">
                    <div class="header-section">
                      
    <footer class="py-5 bg-dark">
        <p class=" m-0 text-center text-white">&copy; shivanshu 2022</p>
    </footer>
    <div class="popup">
        <div class='cnt223'>
            <h1 class="text-warning text-center mb-4">Disclaimer</h1>
            <li>Let me tell you that there is no database of this website.
            </li>
            <li>If you have any problem with this website then please contact me.
            </li>
            <br />
            <p class="mb-4 text-center text-info">Email :- shivanshuraikwar@gmail.com</p>
			<p class="mb-4 text-center text-info">phone no :- 7905976103</p>
            <div class="text-center mb-2"> <button class="close btn btn-primary">CLOSE</button>
            </div>
        </div>
    </div>
    <script>
        $(document).ready(function () {
            $(window).on('load', function () {
                $('#loader').fadeOut();
            });
            var overlay = $('<div id="overlay"></div>');
            overlay.appendTo(document.body);
            overlay.show();
            $(".popup").show();
            $('.close').click(function () {
                $('.popup').hide();
                overlay.appendTo(document.body).remove();
                return false;
            });
            $("#download_admitcard").click(function () {
                let enroll = $("#enroll").val();
                if (enroll.length == 0 || enroll.length < 15) {
                    alert("Please enter your enrollment number");
                    return false;
                }
                else {
                    let link = "https://bteup.ac.in/AdmitCardVerificationCard/AdmitCard/" + enroll.slice(3, 7) + "/" + enroll + ".pdf";
                    $("#download_admitcard").attr("href", link);
                    $("#download_admitcard").attr('target', '_blank');
                    $("#download_admitcard").attr('download', enroll + ".pdf");
                    $("#download_admitcard").click();
                }

            })

        });
    </script>
</body>

</html>
