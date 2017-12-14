# How to Deal with Differents Verbs in the same Method
<br>**Just a simple trick...**<br>

        [Route("UseBoth")]
        public JsonResult UseBoth()
        {
            switch (HttpContext.Request.Method.ToUpperInvariant())
            {
                case "GET":
                    return Json("Deal with Get Request");
                case "POST":
                    return Json("Deal with Post Request");
                default:
                    return Json("Unknown Verb: " + HttpContext.Request.Method);
            }
        }
