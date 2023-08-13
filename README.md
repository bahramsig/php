# php
@extends('layout.home')
@section('content')
    <div class="row">


        <h1 class="alert alert-primary">resturant </h1>
        <div class="container ">
            @foreach ($resturants as $item)
                <div class="card mt-3 ms-1" style="width: 15rem">



                    <div class="card container " style="width: 15rem">
                        <div class="card-body ">
                            <div class="row">
                                <a href={{ route('resturants', ['id' => $item->id]) }}>
                                    <h5 class="card-title">
                                        {{ $item->titel }}
                                    </h5>
                                </a>

                                <img src="{{ asset('img/' . $item->image . '.jpg') }}" width="200" height="100">
                                <p class="card-text">
                                    {{ $item->address }}
                                </p>
                            </div>
                        </div>

                    </div>

                </div>
            @endforeach
        </div>

    </div>
@endsection
