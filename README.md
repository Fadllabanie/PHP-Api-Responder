# Api Responder

ApiResponder Traits for facility when build a laravel Restful Api 

## Installation

Use the File Traits in Base Controller Laravel

## Usage

```PHP Lravel

use App\Http\Traits\ApiResponder;

class Controller extends BaseController
{
    use ApiResponder;
}


## Example 

public function register(RegisterRequest $request)
    {
        $token = $request->store();

        SendVerifyMail::dispatch($request->email, $token);

        return $this->successStatus(__("Send Email"));
    }

